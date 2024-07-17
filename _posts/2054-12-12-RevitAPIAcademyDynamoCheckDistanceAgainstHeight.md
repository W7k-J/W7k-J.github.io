---
layout: post  
title: RevitAPI Academy Coding for Dynamo in C# vs Python CheckDistanceAgainstHeight

date: 2024-07-17 12:00:00
author: Julian
---
![PostPage](/images/2024_BlogPost/Academy_2.jpg)

<!--excerpt-->

One morning, while scrolling through LinkedIn, I stumbled upon a post asking for help with creating a script in Dynamo for Revit. 

![LinkedIn InitialPost](/images/2024_BlogPost/Academy_2_Linkedin_1.jpg)

I initially thought it was a straightforward problem to solve and shared some advices about how to do it. 

![LinkedIn Response](/images/2024_BlogPost/Academy_2_Linkedin_2.jpg)

In the end I decided to do some "speed coding" to solve this problem.  When it comes to prototyping code, I find myself gravitating toward C#. Its seamless integration with the Revit API and OOP help me think in a logical way. I prefer it to Nodes in Dynamo -  especially where 3d geometry is not involved.  

But firstly I had to create a playground to test my future solution. Nothing fancy - simple families with "H" parameter for height.  

![Custom code block](/images/2024_BlogPost/Academy_2_workingSpace.png)

After some thinking which was longer then I expected I started coding.

As a result I created this custom node.

![Custom code block](/images/2024_BlogPost/Academy_2_checkAgainst1.png)

It is not only checking the distances between the elements in correlation to its height but also provides detailed information about problematic elements. Additionally it gives you a human readable report.  
  
So you have everything you need:
* mask for your initial list, 
* report,
* list of lists with problematic elements for each element. 

Sharing the code in C# is not the most straightforward thing to do - yes I need to create my own library at one point.  Since I am proficient in Python, I decided to  rewrite the code for it.  

This way you may not only use both, but also compare them. They are very similar so knowing one will allow you to understand the second snippet. 

The code in C#:

```c#
[MultiReturn(new[] { "Report", "AreElementsOK", "ProblematicWith" })]
public static Dictionary<string, object> CheckDistanceAgainstHeight(List<Revit.Elements.Element> elements, double multiplier, string parameterName)
{
    //INPUTS
    List<Autodesk.Revit.DB.Element> elementsRevitAPI = (from s in elements select s.InternalElement).ToList();

    //OUTPUTS
    List<string> report = new List<String>() { };
    List<bool> areElementsOK = new List<bool>() { };
    List<List<Revit.Elements.Element>> problematicWith = new List<List<Revit.Elements.Element>>() { };

    //ACTION   
    foreach (Autodesk.Revit.DB.Element element in elementsRevitAPI)
    {
        bool maskTemp = true;
        List<Revit.Elements.Element> tempListForOneElement = new List<Revit.Elements.Element> { };

        try
        {
            //GET HEIGHT & LOCATION 
            double elementHeight;

            Autodesk.Revit.DB.Parameter param = element.LookupParameter(parameterName);
            param ??= ((Autodesk.Revit.DB.FamilyInstance)element).Symbol.LookupParameter(parameterName);

            if (param is null) { throw new NullReferenceException("We can't find the Height Parameter"); }

            elementHeight = param.AsDouble();

            XYZ locationPointElement = ((LocationPoint)element.Location).Point;

            //CHECK AGAINST ALL SELECTED
            foreach (Autodesk.Revit.DB.Element elementSecond in elementsRevitAPI)
            {
                if (element.Id == elementSecond.Id)
                    continue;

                XYZ locationPointSecondElement = ((LocationPoint)elementSecond.Location).Point;

                double distance = DistanceToFlat2D(locationPointElement, locationPointSecondElement);

                if (elementHeight * multiplier > distance)
                {
                    maskTemp = false;
                    report.Add($"Element with Id:{element.Id} is too close to Id:{elementSecond.Id}. H = {elementHeight}, Distance = {distance}");
                    tempListForOneElement.Add(elementSecond.ToDSType(true));
                }
            }
        }
        catch 
        {
            maskTemp = false;
        }
        //END VALUES FOR ELEMENT
        areElementsOK.Add(maskTemp);
        problematicWith.Add(tempListForOneElement);
    }

    return new Dictionary<string, object>
    {
        {"Report", report },
        {"AreElementsOK", areElementsOK},
        {"ProblematicWith", problematicWith}
    };
}
public static double DistanceToFlat2D(XYZ point1, XYZ point2)
{
    double flatDistance = new XYZ(point1.X, point1.Y, 0).DistanceTo(new XYZ(point2.X, point2.Y, 0));

    return flatDistance;
}

```

And here goes the code in Python:

```Python
# Boilerplate
import clr
import sys
import System
from System import Array
from System.Collections.Generic import *
clr.AddReference('ProtoGeometry')
from Autodesk.DesignScript.Geometry import *
clr.AddReference("RevitNodes")
import Revit
clr.ImportExtensions(Revit.Elements)
clr.ImportExtensions(Revit.GeometryConversion)
clr.AddReference("RevitServices")
import RevitServices
from RevitServices.Persistence import DocumentManager 
from RevitServices.Transactions import TransactionManager 

clr.AddReference("RevitAPI")
clr.AddReference("RevitAPIUI")

import Autodesk 
from Autodesk.Revit.DB import *
from Autodesk.Revit.UI import *

doc = DocumentManager.Instance.CurrentDBDocument
uiapp = DocumentManager.Instance.CurrentUIApplication 
app = uiapp.Application 
uidoc = uiapp.ActiveUIDocument

# The inputs to this node will be stored as a list in the IN variables.
dataEnteringNode = IN

# Place your code below this line

# INPUTS
elements_revit_api = UnwrapElement(IN[0])
multiplier = IN[1]
parameter_name = IN[2]

# OUTPUTS
report = []
are_elements_ok = []
problematic_with = []

# ACTION
for element in elements_revit_api:
    
    mask_temp = True
    temp_list_for_one_element = []
    
    try:
        # GET HEIGHT & LOCATION
        param = element.LookupParameter(parameter_name)
        
        if param is None:
            param = element.Symbol.LookupParameter(parameter_name)
        if param is None:
            raise ValueError("We can't find the Height Parameter")
            
        element_height = param.AsDouble()
        location_point_element = element.Location.Point
        
        # CHECK AGAINST ALL SELECTED
        for element_second in elements_revit_api:
            if element.Id == element_second.Id:
                continue
                
            location_point_second_element = element_second.Location.Point
            
            flat_distance = XYZ(location_point_element.X, location_point_element.Y, 0).DistanceTo(XYZ(location_point_second_element.X, location_point_second_element.Y, 0))
            
            if element_height * multiplier > flat_distance:
                mask_temp = False
                
                report.append("Element with Id:{element.Id} is too close to Id:{element_second.Id}. H = {element_height}, Distance = {distance}")
                
                temp_list_for_one_element.append(element_second.ToDSType(True))
    except:
        mask_temp = False
        
    # END VALUES FOR ELEMENT
    are_elements_ok.append(mask_temp)
    problematic_with.append(temp_list_for_one_element)

# Assign your output to the OUT variable.
OUT = [report, are_elements_ok, problematic_with]

```