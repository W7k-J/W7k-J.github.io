---
layout: page
title: Leveler
permalink: /tools/leveler/
---

![MainTab](/images/Tools/Leveler/LevelerTab.png)

The purpose of this tool is to allow you to change reference levels without changing element's location / elevation. The tool is going to do it automatically. It will set correct offsets for you. 

No longer, you will have to manually calculate them. Simply choose new level (or use other provided option) and it will be done. Moreover, because the tool changes the offsets and levels at the same time your Revit model will not explode in the process. 

## Who should use this tool?

This tool was created with Revit Modellers in mind. It easily saves them countless hours each year. 

I came out with the idea of this tool when I had to change manually references of almost all elements in the projects. This tiny tool would save us at least 2 weeks of work.  

[Link to the Autodesk App Store](https://apps.autodesk.com/RVT/en/Detail/Index?id=7992073470185484796&appLang=en&os=Win64)

## Leveler Version 1.1

The tool will be updated with 10 more scripts. You will find some extra information about them here.  

## Buttons by Options

![LevelerExtendedOptions](/images/Tools/Leveler/LevelerExtendedOptions.png)

Each of the buttons has 6 different option you might use.   

### Default  

![FloorsLToSL](/images/Tools/Leveler/FloorsLToSL.png)
![RoofsLToSL](/images/Tools/Leveler/RoofsLToSL.png)
![CeilingsLToSL](/images/Tools/Leveler/CeilingsLToSL.png)
![PadsLToSL](/images/Tools/Leveler/PadsLToSL.png)
![VariousLToSL](/images/Tools/Leveler/VariousLToSL.png)
![WallsLToSLT](/images/Tools/Leveler/WallsLToSLT.png)
![WallsLToSLB](/images/Tools/Leveler/WallsLToSLB.png)
![ColumnsLToSLT](/images/Tools/Leveler/ColumnsLToSLT.png)
![ColumnsLToSLB](/images/Tools/Leveler/ColumnsLToSLB.png)
![VariousLToSLT](/images/Tools/Leveler/VariousLToSLT.png)
![VariousLToSLB](/images/Tools/Leveler/VariousLToSLB.png)
![WindowsLToSL](/images/Tools/Leveler/WindowsLToSL.png)
![DoorsLToSL](/images/Tools/Leveler/DoorsLToSL.png)
![CWindowsLToSL](/images/Tools/Leveler/CWindowsLToSL.png)
![CDoorsLToSL](/images/Tools/Leveler/CDoorsLToSL.png)
  
  
You will be prompted to choose <b>one level</b> and the tool will try to set it for all selected elements:  
   
![LevelerSelection](/images/Tools/Leveler/LevelerSelection.png)

### Set level to the Closest 

![FloorsLToCL](/images/Tools/Leveler/FloorsLToCL.png)
![RoofsLToCL](/images/Tools/Leveler/RoofsLToCL.png)
![CeilingsLToCL](/images/Tools/Leveler/CeilingsLToCL.png)
![PadsLToCL](/images/Tools/Leveler/PadsLToCL.png)
![VariousLToCL](/images/Tools/Leveler/VariousLToCL.png)
![WallsLToCLT](/images/Tools/Leveler/WallsLToCLT.png)
![WallsLToCLB](/images/Tools/Leveler/WallsLToCLB.png)
![ColumnsLToCLT](/images/Tools/Leveler/ColumnsLToCLT.png)
![ColumnsLToCLB](/images/Tools/Leveler/ColumnsLToCLB.png)
![VariousLToCLT](/images/Tools/Leveler/VariousLToCLT.png)
![VariousLToCLB](/images/Tools/Leveler/VariousLToCLB.png)
![WindowsLToCL](/images/Tools/Leveler/WindowsLToCL.png)
![DoorsLToCL](/images/Tools/Leveler/DoorsLToCL.png)
![CWindowsLToCL](/images/Tools/Leveler/CWindowsLToCL.png)
![CDoorsLToCL](/images/Tools/Leveler/CDoorsLToCL.png)

The tool will automatically choose <b>the closest level</b> (the one which will result in the smallest offset) for each selected elements.  

The levels will be calculated separately for all selected elements.

### Set level to the Closest Above

![FloorsLToCA](/images/Tools/Leveler/FloorsLToCA.png)
![RoofsLToCA](/images/Tools/Leveler/RoofsLToCA.png)
![CeilingsLToCA](/images/Tools/Leveler/CeilingsLToCA.png)
![PadsLToCA](/images/Tools/Leveler/PadsLToCA.png)
![VariousLToCA](/images/Tools/Leveler/VariousLToCA.png)
![WallsLToCAT](/images/Tools/Leveler/WallsLToCAT.png)
![WallsLToCAB](/images/Tools/Leveler/WallsLToCAB.png)
![ColumnsLToCAT](/images/Tools/Leveler/ColumnsLToCAT.png)
![ColumnsLToCAB](/images/Tools/Leveler/ColumnsLToCAB.png)
![VariousLToCAT](/images/Tools/Leveler/VariousLToCAT.png)
![VariousLToCAB](/images/Tools/Leveler/VariousLToCAB.png)
![WindowsLToCA](/images/Tools/Leveler/WindowsLToCA.png)
![DoorsLToCA](/images/Tools/Leveler/DoorsLToCA.png)
![CWindowsLToCA](/images/Tools/Leveler/CWindowsLToCA.png)
![CDoorsLToCA](/images/Tools/Leveler/CDoorsLToCA.png)

Similarly, The tool will automatically choose the closest level for your elements, but this time it will look only for a level which elevation is above the selected elements. 
The levels will be calculated separately for all selected elements.

<i>For example:  
if you have a floor between two levels, the tool will always assign the level above your floor - even if the offset would be comparable larger than to the level below. </i>


### Set level to the Closest Below

![FloorsLToCB](/images/Tools/Leveler/FloorsLToCB.png)
![RoofsLToCB](/images/Tools/Leveler/RoofsLToCB.png)
![CeilingsLToCB](/images/Tools/Leveler/CeilingsLToCB.png)
![PadsLToCB](/images/Tools/Leveler/PadsLToCB.png)
![VariousLToCB](/images/Tools/Leveler/VariousLToCB.png)
![WallsLToCBT](/images/Tools/Leveler/WallsLToCBT.png)
![WallsLToCBB](/images/Tools/Leveler/WallsLToCBB.png)
![ColumnsLToCBT](/images/Tools/Leveler/ColumnsLToCBT.png)
![ColumnsLToCBB](/images/Tools/Leveler/ColumnsLToCBB.png)
![VariousLToCBT](/images/Tools/Leveler/VariousLToCBT.png)
![VariousLToCBB](/images/Tools/Leveler/VariousLToCBB.png)
![WindowsLToCB](/images/Tools/Leveler/WindowsLToCB.png)
![DoorsLToCB](/images/Tools/Leveler/DoorsLToCB.png)
![CWindowsLToCB](/images/Tools/Leveler/CWindowsLToCB.png)
![CDoorsLToCB](/images/Tools/Leveler/CDoorsLToCB.png)

Similarly, The tool will automatically choose the closest level for your elements, but this time it will look only for a level which elevation is below the selected elements. 
The levels will be calculated separately for all selected elements.

<i>For example:  
if you have a floor between two levels, the tool will always assign the level below your floor - even if the offset would be comparable larger than to the level above.</i>

### Set level to the one above currently selected 

![FloorsLToOA](/images/Tools/Leveler/FloorsLToOA.png)
![RoofsLToOA](/images/Tools/Leveler/RoofsLToOA.png)
![CeilingsLToOA](/images/Tools/Leveler/CeilingsLToOA.png)
![PadsLToOA](/images/Tools/Leveler/PadsLToOA.png)
![VariousLToOA](/images/Tools/Leveler/VariousLToOA.png)
![WallsLToOAT](/images/Tools/Leveler/WallsLToOAT.png)
![WallsLToOAB](/images/Tools/Leveler/WallsLToOAB.png)
![ColumnsLToOAT](/images/Tools/Leveler/ColumnsLToOAT.png)
![ColumnsLToOAB](/images/Tools/Leveler/ColumnsLToOAB.png)
![VariousLToOAT](/images/Tools/Leveler/VariousLToOAT.png)
![VariousLToOAB](/images/Tools/Leveler/VariousLToOAB.png)
![WindowsLToOA](/images/Tools/Leveler/WindowsLToOA.png)
![DoorsLToOA](/images/Tools/Leveler/DoorsLToOA.png)
![CWindowsLToOA](/images/Tools/Leveler/CWindowsLToOA.png)
![CDoorsLToOA](/images/Tools/Leveler/CDoorsLToOA.png)

The tool will automatically change the reference level to one above currently selected.
The levels will be calculated separately for all selected elements.

<i>For example:  
if you have a floor on level 1, it will change its reference to level 2 and its offset to -3000 mm. </i>


### Set level to the one below currently selected 

![FloorsLToOB](/images/Tools/Leveler/FloorsLToOB.png)
![RoofsLToOB](/images/Tools/Leveler/RoofsLToOB.png)
![CeilingsLToOB](/images/Tools/Leveler/CeilingsLToOB.png)
![PadsLToOB](/images/Tools/Leveler/PadsLToOB.png)
![VariousLToOB](/images/Tools/Leveler/VariousLToOB.png)
![WallsLToOBT](/images/Tools/Leveler/WallsLToOBT.png)
![WallsLToOBB](/images/Tools/Leveler/WallsLToOBB.png)
![ColumnsLToOBT](/images/Tools/Leveler/ColumnsLToOBT.png)
![ColumnsLToOBB](/images/Tools/Leveler/ColumnsLToOBB.png)
![VariousLToOBT](/images/Tools/Leveler/VariousLToOBT.png)
![VariousLToOBB](/images/Tools/Leveler/VariousLToOBB.png)
![WindowsLToOB](/images/Tools/Leveler/WindowsLToOB.png)
![DoorsLToOB](/images/Tools/Leveler/DoorsLToOB.png)
![CWindowsLToOB](/images/Tools/Leveler/CWindowsLToOB.png)
![CDoorsLToOB](/images/Tools/Leveler/CDoorsLToOB.png)

The tool will automatically change the reference level to one above currently selected. 
The levels will be calculated separately for all selected elements.

<i>For example:  
if you have a floor on level 2, it will change its reference to level 1 and its offset to 3000 mm. </i>

## Buttons by elements

Please find below a short description with information how each category works. We also included some information about limitations of this tool. 
By default the tool filters out all model-in-place families. 

## Levels - Objects With One Reference
![MainTab](/images/Tools/Leveler/LevelerTabOneRef.png)
  
This tab contains tools for elements with one reference level. 

### Floors  

![FloorsLToSL](/images/Tools/Leveler/FloorsLToSL.png)
![FloorsLToCL](/images/Tools/Leveler/FloorsLToCL.png)
![FloorsLToCA](/images/Tools/Leveler/FloorsLToCA.png)
![FloorsLToCB](/images/Tools/Leveler/FloorsLToCB.png)
![FloorsLToOA](/images/Tools/Leveler/FloorsLToOA.png)
![FloorsLToOB](/images/Tools/Leveler/FloorsLToOB.png)  

Works on default system floors. 

### Roofs  

![RoofsLToSL](/images/Tools/Leveler/RoofsLToSL.png)
![RoofsLToCL](/images/Tools/Leveler/RoofsLToCL.png)
![RoofsLToCA](/images/Tools/Leveler/RoofsLToCA.png)
![RoofsLToCB](/images/Tools/Leveler/RoofsLToCB.png)
![RoofsLToOA](/images/Tools/Leveler/RoofsLToOA.png)
![RoofsLToOB](/images/Tools/Leveler/RoofsLToOB.png)
  
Works on all 3 different system roofs (Roof by footprint, Roof by Extrusion and Roof by Face)

### Ceilings  

![CeilingsLToSL](/images/Tools/Leveler/CeilingsLToSL.png)
![CeilingsLToCL](/images/Tools/Leveler/CeilingsLToCL.png)
![CeilingsLToCA](/images/Tools/Leveler/CeilingsLToCA.png)
![CeilingsLToCB](/images/Tools/Leveler/CeilingsLToCB.png)
![CeilingsLToOA](/images/Tools/Leveler/CeilingsLToOA.png)
![CeilingsLToOB](/images/Tools/Leveler/CeilingsLToOB.png)

Works on standard system ceilings.

### Pads (for older versions of Revit (pre-2024))

![PadsLToSL](/images/Tools/Leveler/PadsLToSL.png)
![PadsLToCL](/images/Tools/Leveler/PadsLToCL.png)
![PadsLToCA](/images/Tools/Leveler/PadsLToCA.png)
![PadsLToCB](/images/Tools/Leveler/PadsLToCB.png)
![PadsLToOA](/images/Tools/Leveler/PadsLToOA.png)
![PadsLToOB](/images/Tools/Leveler/PadsLToOB.png)

Works on building pads. This function is included only in versions up to 2023.  

### Experimental! Various With One Reference  

![VariousLToSL](/images/Tools/Leveler/VariousLToSL.png)
![VariousLToCL](/images/Tools/Leveler/VariousLToCL.png)
![VariousLToCA](/images/Tools/Leveler/VariousLToCA.png)
![VariousLToCB](/images/Tools/Leveler/VariousLToCB.png)
![VariousLToOA](/images/Tools/Leveler/VariousLToOA.png)
![VariousLToOB](/images/Tools/Leveler/VariousLToOB.png)

It is an experimental option.
In theory it should works on many categories but right now it is limited to:

Structural Fundations
Reavels  
Wall Sweeps
Furiture
Parkings
Mechanical Equipement
Ligting fixtrures
Plumbing fixtures
Generic models


Please inform us if you see any problems or would like us to include another category of objects to it. Adding more categories is on our ToDo list. 

## Levels - Objects With Two References

![MainTab](/images/Tools/Leveler/LevelerTabTwoRef.png)
  
This tab contains tools for elements with two reference levels (Top and Bottom). The tool is also allowing to select <b> Unconnected Level </b> for them. 

### Walls

#### Bottom
![WallsLToSLT](/images/Tools/Leveler/WallsLToSLB.png)
![WallsLToCLT](/images/Tools/Leveler/WallsLToCLB.png)
![WallsLToCAT](/images/Tools/Leveler/WallsLToCAB.png)
![WallsLToCBT](/images/Tools/Leveler/WallsLToCBB.png)
![WallsLToOAT](/images/Tools/Leveler/WallsLToOAB.png)
![WallsLToOBT](/images/Tools/Leveler/WallsLToOBB.png)

#### Top
![WallsLToSLT](/images/Tools/Leveler/WallsLToSLT.png)
![WallsLToCLT](/images/Tools/Leveler/WallsLToCLT.png)
![WallsLToCAT](/images/Tools/Leveler/WallsLToCAT.png)
![WallsLToCBT](/images/Tools/Leveler/WallsLToCBT.png)
![WallsLToOAT](/images/Tools/Leveler/WallsLToOAT.png)
![WallsLToOBT](/images/Tools/Leveler/WallsLToOBT.png)

Works on system walls and curtain walls. 

### Columns  

#### Bottom
![ColumnsLToSLB](/images/Tools/Leveler/ColumnsLToSLB.png)
![ColumnsLToCLB](/images/Tools/Leveler/ColumnsLToCLB.png)
![ColumnsLToCAB](/images/Tools/Leveler/ColumnsLToCAB.png)
![ColumnsLToCBB](/images/Tools/Leveler/ColumnsLToCBB.png)
![ColumnsLToOAB](/images/Tools/Leveler/ColumnsLToOAB.png)
![ColumnsLToOBB](/images/Tools/Leveler/ColumnsLToOBB.png)

#### Top
![ColumnsLToSLT](/images/Tools/Leveler/ColumnsLToSLT.png)
![ColumnsLToCLT](/images/Tools/Leveler/ColumnsLToCLT.png)
![ColumnsLToCAT](/images/Tools/Leveler/ColumnsLToCAT.png)
![ColumnsLToCBT](/images/Tools/Leveler/ColumnsLToCBT.png)
![ColumnsLToOAT](/images/Tools/Leveler/ColumnsLToOAT.png)
![ColumnsLToOBT](/images/Tools/Leveler/ColumnsLToOBT.png)

Works on architectural and structural columns. 

### Experimental! Various With Two References

#### Bottom
![VariousLToSLB](/images/Tools/Leveler/VariousLToSLB.png)
![VariousLToCLB](/images/Tools/Leveler/VariousLToCLB.png)
![VariousLToCAB](/images/Tools/Leveler/VariousLToCAB.png)
![VariousLToCBB](/images/Tools/Leveler/VariousLToCBB.png)
![VariousLToOAB](/images/Tools/Leveler/VariousLToOAB.png)
![VariousLToOBB](/images/Tools/Leveler/VariousLToOBB.png)

#### Top
![VariousLToSLT](/images/Tools/Leveler/VariousLToSLT.png)
![VariousLToCLT](/images/Tools/Leveler/VariousLToCLT.png)
![VariousLToCAT](/images/Tools/Leveler/VariousLToCAT.png)
![VariousLToCBT](/images/Tools/Leveler/VariousLToCBT.png)
![VariousLToOAT](/images/Tools/Leveler/VariousLToOAT.png)
![VariousLToOBT](/images/Tools/Leveler/VariousLToOBT.png)

It is an experimental option.
Works on many categories and because of that it is really hard to include all scenarious. Should be fine, but please inform us if you see any problems or would like us to include another category of objects.

Works on:  
Generic Families  
Shafts  
Straight Wall Openings   
Stairs  
Ramps  
etc.  

### Things to keep in mind:  
<strong>2 level based families</strong> - Top Level can't be set to "Unconnected". It is default Revit limitation so we can't do anything about it. I didn't know about it too.  
  
<strong>Ramps</strong> - Ramps are broken in Revit - For more info visit:  
<a href="https://w7k.pl//knowledge/revit/ramps/">Revit Ramps</a>  
In short : Please don't select "Unconnected" and do not use the tool on ramps where level is set to "None".   

## Levels - Other Objects  

![MainTab](/images/Tools/Leveler/LevelerTabOther.png)

### Doors  

![DoorsLToSL](/images/Tools/Leveler/DoorsLToSL.png)
![DoorsLToCL](/images/Tools/Leveler/DoorsLToCL.png)
![DoorsLToCA](/images/Tools/Leveler/DoorsLToCA.png)
![DoorsLToCB](/images/Tools/Leveler/DoorsLToCB.png)
![DoorsLToOA](/images/Tools/Leveler/DoorsLToOA.png)
![DoorsLToOB](/images/Tools/Leveler/DoorsLToOB.png)

Works on standard door families hosted on the walls. 

### Windows  

![WindowsLToSL](/images/Tools/Leveler/WindowsLToSL.png)
![WindowsLToCL](/images/Tools/Leveler/WindowsLToCL.png)
![WindowsLToCA](/images/Tools/Leveler/WindowsLToCA.png)
![WindowsLToCB](/images/Tools/Leveler/WindowsLToCB.png)
![WindowsLToOA](/images/Tools/Leveler/WindowsLToOA.png)
![WindowsLToOB](/images/Tools/Leveler/WindowsLToOB.png)

Works on standard window families hosted on the walls. 

### Experimental! Curtain Doors  
  
![CDoorsLToSL](/images/Tools/Leveler/CDoorsLToSL.png)
![CDoorsLToCL](/images/Tools/Leveler/CDoorsLToCL.png)
![CDoorsLToCA](/images/Tools/Leveler/CDoorsLToCA.png)
![CDoorsLToCB](/images/Tools/Leveler/CDoorsLToCB.png)
![CDoorsLToOA](/images/Tools/Leveler/CDoorsLToOA.png)
![CDoorsLToOB](/images/Tools/Leveler/CDoorsLToOB.png)

It is an experimental option. 

Did you know that Revit API allows you to change the level of curtain panel doors? It is a highly experimental option, so use it wisely. One thing to keep in mind is that editing curtain wall sometimes overwrites these settings back to default ones (base of curtain wall).

### Experimental! Curtain Windows  
  
![CWindowsLToSL](/images/Tools/Leveler/CWindowsLToSL.png)
![CWindowsLToCL](/images/Tools/Leveler/CWindowsLToCL.png)
![CWindowsLToCA](/images/Tools/Leveler/CWindowsLToCA.png)
![CWindowsLToCB](/images/Tools/Leveler/CWindowsLToCB.png)
![CWindowsLToOA](/images/Tools/Leveler/CWindowsLToOA.png)
![CWindowsLToOB](/images/Tools/Leveler/CWindowsLToOB.png)

It is an experimental option. 

Did you know that Revit API allows you to change the level of curtain panel windows? It is a highly experimental option, so use it wisely. One thing to keep in mind is that editing curtain wall sometimes overwrites these settings back to default ones (base of curtain wall).

# Video

<div>
  <div style="position:relative;padding-top:56.25%;">
    <iframe src="https://www.youtube.com/embed/cXdXycnS-VA" frameborder="0" allowfullscreen
      style="position:absolute;top:0;left:0;width:100%;height:100%;"></iframe>
  </div>
</div>

## Versions
Version 1.0 was published at 2023-10-18. Works on Autodesk Revit 2020 - 2024

<br>
<div class="backToTools">
    <a href="https://w7k.pl/tools/">Go Back to W7k Tools</a>
</div>
<div class="terms">
    <a href="https://w7k.pl/terms/">Disclaimers, Policies, Terms & Conditions</a>
</div>


{% include disqus.html %} 