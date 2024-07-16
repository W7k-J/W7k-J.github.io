---
layout: post  
title: RevitAPI Academy Coding for Dynamo in C# vs Python

date: 2054-12-12 12:00:00
author: Julian
---
![PostPage](/images/2024_BlogPost/AutodeskDevCon2024.jpg)

<!--excerpt-->


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