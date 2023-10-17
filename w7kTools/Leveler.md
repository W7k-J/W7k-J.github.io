---
layout: page
title: Leveler
permalink: /tools/leveler/
---

![MainTab](/images/Tools/LevelChanger/LevelChangerTab.png)

The purpose of this tool is to allow you to change reference levels without changing element's location / elevation. The tool is going to do it automatically. It will set correct offsets for you. 

No longer, you will have to manually calculate them. Simply choose new level (or use other provided option) and it will be done. Moreover, because the tool changes the offsets and levels at the same time your Revit model will not explode in the process. 

## Who should use this tool?

This tool was created with Revit Modellers in mind. It easily saves them countless hours each year. 

I came out with the idea of this tool when I had to change manually references of almost all elements in the projects. This tiny tool would save us at least 2 weeks of work.  

## Buttons by Options

![LevelChangerExtendedOptions](/images/Tools/LevelChanger/LevelChangerExtendedOptions.png)

Each of the buttons has 6 different option you might use.   

### Default  

![FloorsLToSL](/images/Tools/LevelChanger/FloorsLToSL.png)
![RoofsLToSL](/images/Tools/LevelChanger/RoofsLToSL.png)
![CeilingsLToSL](/images/Tools/LevelChanger/CeilingsLToSL.png)
![PadsLToSL](/images/Tools/LevelChanger/PadsLToSL.png)
![VariousLToSL](/images/Tools/LevelChanger/VariousLToSL.png)
![WallsLToSLT](/images/Tools/LevelChanger/WallsLToSLT.png)
![WallsLToSLB](/images/Tools/LevelChanger/WallsLToSLB.png)
![ColumnsLToSLT](/images/Tools/LevelChanger/ColumnsLToSLT.png)
![ColumnsLToSLB](/images/Tools/LevelChanger/ColumnsLToSLB.png)
![VariousLToSLT](/images/Tools/LevelChanger/VariousLToSLT.png)
![VariousLToSLB](/images/Tools/LevelChanger/VariousLToSLB.png)
![WindowsLToSL](/images/Tools/LevelChanger/WindowsLToSL.png)
![DoorsLToSL](/images/Tools/LevelChanger/DoorsLToSL.png)
![CWindowsLToSL](/images/Tools/LevelChanger/CWindowsLToSL.png)
![CDoorsLToSL](/images/Tools/LevelChanger/CDoorsLToSL.png)
  
  
You will be prompted to choose <b>one level</b> and the tool will try to set it for all selected elements:  
   
![LevelChangerSelection](/images/Tools/LevelChanger/LevelChangerSelection.png)

### Set level to the Closest 

![FloorsLToCL](/images/Tools/LevelChanger/FloorsLToCL.png)
![RoofsLToCL](/images/Tools/LevelChanger/RoofsLToCL.png)
![CeilingsLToCL](/images/Tools/LevelChanger/CeilingsLToCL.png)
![PadsLToCL](/images/Tools/LevelChanger/PadsLToCL.png)
![VariousLToCL](/images/Tools/LevelChanger/VariousLToCL.png)
![WallsLToCLT](/images/Tools/LevelChanger/WallsLToCLT.png)
![WallsLToCLB](/images/Tools/LevelChanger/WallsLToCLB.png)
![ColumnsLToCLT](/images/Tools/LevelChanger/ColumnsLToCLT.png)
![ColumnsLToCLB](/images/Tools/LevelChanger/ColumnsLToCLB.png)
![VariousLToCLT](/images/Tools/LevelChanger/VariousLToCLT.png)
![VariousLToCLB](/images/Tools/LevelChanger/VariousLToCLB.png)
![WindowsLToCL](/images/Tools/LevelChanger/WindowsLToCL.png)
![DoorsLToCL](/images/Tools/LevelChanger/DoorsLToCL.png)
![CWindowsLToCL](/images/Tools/LevelChanger/CWindowsLToCL.png)
![CDoorsLToCL](/images/Tools/LevelChanger/CDoorsLToCL.png)

The tool will automatically choose <b>the closest level</b> (the one which will result in the smallest offset) for each selected elements.  

The levels will be calculated separately for all selected elements.

### Set level to the Closest Above

![FloorsLToCA](/images/Tools/LevelChanger/FloorsLToCA.png)
![RoofsLToCA](/images/Tools/LevelChanger/RoofsLToCA.png)
![CeilingsLToCA](/images/Tools/LevelChanger/CeilingsLToCA.png)
![PadsLToCA](/images/Tools/LevelChanger/PadsLToCA.png)
![VariousLToCA](/images/Tools/LevelChanger/VariousLToCA.png)
![WallsLToCAT](/images/Tools/LevelChanger/WallsLToCAT.png)
![WallsLToCAB](/images/Tools/LevelChanger/WallsLToCAB.png)
![ColumnsLToCAT](/images/Tools/LevelChanger/ColumnsLToCAT.png)
![ColumnsLToCAB](/images/Tools/LevelChanger/ColumnsLToCAB.png)
![VariousLToCAT](/images/Tools/LevelChanger/VariousLToCAT.png)
![VariousLToCAB](/images/Tools/LevelChanger/VariousLToCAB.png)
![WindowsLToCA](/images/Tools/LevelChanger/WindowsLToCA.png)
![DoorsLToCA](/images/Tools/LevelChanger/DoorsLToCA.png)
![CWindowsLToCA](/images/Tools/LevelChanger/CWindowsLToCA.png)
![CDoorsLToCA](/images/Tools/LevelChanger/CDoorsLToCA.png)

Similarly, The tool will automatically choose the closest level for your elements, but this time it will look only for a level which elevation is above the selected elements. 
The levels will be calculated separately for all selected elements.

<i>For example:  
if you have a floor between two levels, the tool will always assign the level above your floor - even if the offset would be comparable larger than to the level below. </i>


### Set level to the Closest Below

![FloorsLToCB](/images/Tools/LevelChanger/FloorsLToCB.png)
![RoofsLToCB](/images/Tools/LevelChanger/RoofsLToCB.png)
![CeilingsLToCB](/images/Tools/LevelChanger/CeilingsLToCB.png)
![PadsLToCB](/images/Tools/LevelChanger/PadsLToCB.png)
![VariousLToCB](/images/Tools/LevelChanger/VariousLToCB.png)
![WallsLToCBT](/images/Tools/LevelChanger/WallsLToCBT.png)
![WallsLToCBB](/images/Tools/LevelChanger/WallsLToCBB.png)
![ColumnsLToCBT](/images/Tools/LevelChanger/ColumnsLToCBT.png)
![ColumnsLToCBB](/images/Tools/LevelChanger/ColumnsLToCBB.png)
![VariousLToCBT](/images/Tools/LevelChanger/VariousLToCBT.png)
![VariousLToCBB](/images/Tools/LevelChanger/VariousLToCBB.png)
![WindowsLToCB](/images/Tools/LevelChanger/WindowsLToCB.png)
![DoorsLToCB](/images/Tools/LevelChanger/DoorsLToCB.png)
![CWindowsLToCB](/images/Tools/LevelChanger/CWindowsLToCB.png)
![CDoorsLToCB](/images/Tools/LevelChanger/CDoorsLToCB.png)

Similarly, The tool will automatically choose the closest level for your elements, but this time it will look only for a level which elevation is below the selected elements. 
The levels will be calculated separately for all selected elements.

<i>For example:  
if you have a floor between two levels, the tool will always assign the level below your floor - even if the offset would be comparable larger than to the level above.</i>

### Set level to the one above currently selected 

![FloorsLToOA](/images/Tools/LevelChanger/FloorsLToOA.png)
![RoofsLToOA](/images/Tools/LevelChanger/RoofsLToOA.png)
![CeilingsLToOA](/images/Tools/LevelChanger/CeilingsLToOA.png)
![PadsLToOA](/images/Tools/LevelChanger/PadsLToOA.png)
![VariousLToOA](/images/Tools/LevelChanger/VariousLToOA.png)
![WallsLToOAT](/images/Tools/LevelChanger/WallsLToOAT.png)
![WallsLToOAB](/images/Tools/LevelChanger/WallsLToOAB.png)
![ColumnsLToOAT](/images/Tools/LevelChanger/ColumnsLToOAT.png)
![ColumnsLToOAB](/images/Tools/LevelChanger/ColumnsLToOAB.png)
![VariousLToOAT](/images/Tools/LevelChanger/VariousLToOAT.png)
![VariousLToOAB](/images/Tools/LevelChanger/VariousLToOAB.png)
![WindowsLToOA](/images/Tools/LevelChanger/WindowsLToOA.png)
![DoorsLToOA](/images/Tools/LevelChanger/DoorsLToOA.png)
![CWindowsLToOA](/images/Tools/LevelChanger/CWindowsLToOA.png)
![CDoorsLToOA](/images/Tools/LevelChanger/CDoorsLToOA.png)

The tool will automatically change the reference level to one above currently selected.
The levels will be calculated separately for all selected elements.

<i>For example:  
if you have a floor on level 1, it will change its reference to level 2 and its offset to -3000 mm. </i>


### Set level to the one below currently selected 

![FloorsLToOB](/images/Tools/LevelChanger/FloorsLToOB.png)
![RoofsLToOB](/images/Tools/LevelChanger/RoofsLToOB.png)
![CeilingsLToOB](/images/Tools/LevelChanger/CeilingsLToOB.png)
![PadsLToOB](/images/Tools/LevelChanger/PadsLToOB.png)
![VariousLToOB](/images/Tools/LevelChanger/VariousLToOB.png)
![WallsLToOBT](/images/Tools/LevelChanger/WallsLToOBT.png)
![WallsLToOBB](/images/Tools/LevelChanger/WallsLToOBB.png)
![ColumnsLToOBT](/images/Tools/LevelChanger/ColumnsLToOBT.png)
![ColumnsLToOBB](/images/Tools/LevelChanger/ColumnsLToOBB.png)
![VariousLToOBT](/images/Tools/LevelChanger/VariousLToOBT.png)
![VariousLToOBB](/images/Tools/LevelChanger/VariousLToOBB.png)
![WindowsLToOB](/images/Tools/LevelChanger/WindowsLToOB.png)
![DoorsLToOB](/images/Tools/LevelChanger/DoorsLToOB.png)
![CWindowsLToOB](/images/Tools/LevelChanger/CWindowsLToOB.png)
![CDoorsLToOB](/images/Tools/LevelChanger/CDoorsLToOB.png)

The tool will automatically change the reference level to one above currently selected. 
The levels will be calculated separately for all selected elements.

<i>For example:  
if you have a floor on level 2, it will change its reference to level 1 and its offset to 3000 mm. </i>

## Buttons by elements

Please find below a short description with information how each category works. We also included some information about limitations of this tool. 
By default the tool filters out all model-in-place families. 

## Levels - Objects With One Reference
![MainTab](/images/Tools/LevelChanger/LevelChangerTabOneRef.png)
  
This tab contains tools for elements with one reference level. 

### Floors  

![FloorsLToSL](/images/Tools/LevelChanger/FloorsLToSL.png)
![FloorsLToCL](/images/Tools/LevelChanger/FloorsLToCL.png)
![FloorsLToCA](/images/Tools/LevelChanger/FloorsLToCA.png)
![FloorsLToCB](/images/Tools/LevelChanger/FloorsLToCB.png)
![FloorsLToOA](/images/Tools/LevelChanger/FloorsLToOA.png)
![FloorsLToOB](/images/Tools/LevelChanger/FloorsLToOB.png)  

Works on default system floors. 

### Roofs  

![RoofsLToSL](/images/Tools/LevelChanger/RoofsLToSL.png)
![RoofsLToCL](/images/Tools/LevelChanger/RoofsLToCL.png)
![RoofsLToCA](/images/Tools/LevelChanger/RoofsLToCA.png)
![RoofsLToCB](/images/Tools/LevelChanger/RoofsLToCB.png)
![RoofsLToOA](/images/Tools/LevelChanger/RoofsLToOA.png)
![RoofsLToOB](/images/Tools/LevelChanger/RoofsLToOB.png)
  
Works on all 3 different system roofs (Roof by footprint, Roof by Extrusion and Roof by Face)

### Ceilings  

![CeilingsLToSL](/images/Tools/LevelChanger/CeilingsLToSL.png)
![CeilingsLToCL](/images/Tools/LevelChanger/CeilingsLToCL.png)
![CeilingsLToCA](/images/Tools/LevelChanger/CeilingsLToCA.png)
![CeilingsLToCB](/images/Tools/LevelChanger/CeilingsLToCB.png)
![CeilingsLToOA](/images/Tools/LevelChanger/CeilingsLToOA.png)
![CeilingsLToOB](/images/Tools/LevelChanger/CeilingsLToOB.png)

Works on standard system ceilings.

### Pads (for older versions of Revit (pre-2024))

![PadsLToSL](/images/Tools/LevelChanger/PadsLToSL.png)
![PadsLToCL](/images/Tools/LevelChanger/PadsLToCL.png)
![PadsLToCA](/images/Tools/LevelChanger/PadsLToCA.png)
![PadsLToCB](/images/Tools/LevelChanger/PadsLToCB.png)
![PadsLToOA](/images/Tools/LevelChanger/PadsLToOA.png)
![PadsLToOB](/images/Tools/LevelChanger/PadsLToOB.png)

Works on building pads. This function is included only in versions up to 2023.  

### Experimental! Various With One Reference  

![VariousLToSL](/images/Tools/LevelChanger/VariousLToSL.png)
![VariousLToCL](/images/Tools/LevelChanger/VariousLToCL.png)
![VariousLToCA](/images/Tools/LevelChanger/VariousLToCA.png)
![VariousLToCB](/images/Tools/LevelChanger/VariousLToCB.png)
![VariousLToOA](/images/Tools/LevelChanger/VariousLToOA.png)
![VariousLToOB](/images/Tools/LevelChanger/VariousLToOB.png)

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

![MainTab](/images/Tools/LevelChanger/LevelChangerTabTwoRef.png)
  
This tab contains tools for elements with two reference levels (Top and Bottom). The tool is also allowing to select <b> Unconnected Level </b> for them. 

### Walls

#### Bottom
![WallsLToSLT](/images/Tools/LevelChanger/WallsLToSLB.png)
![WallsLToCLT](/images/Tools/LevelChanger/WallsLToCLB.png)
![WallsLToCAT](/images/Tools/LevelChanger/WallsLToCAB.png)
![WallsLToCBT](/images/Tools/LevelChanger/WallsLToCBB.png)
![WallsLToOAT](/images/Tools/LevelChanger/WallsLToOAB.png)
![WallsLToOBT](/images/Tools/LevelChanger/WallsLToOBB.png)

#### Top
![WallsLToSLT](/images/Tools/LevelChanger/WallsLToSLT.png)
![WallsLToCLT](/images/Tools/LevelChanger/WallsLToCLT.png)
![WallsLToCAT](/images/Tools/LevelChanger/WallsLToCAT.png)
![WallsLToCBT](/images/Tools/LevelChanger/WallsLToCBT.png)
![WallsLToOAT](/images/Tools/LevelChanger/WallsLToOAT.png)
![WallsLToOBT](/images/Tools/LevelChanger/WallsLToOBT.png)

Works on system walls and curtain walls. 

### Columns  

#### Bottom
![ColumnsLToSLB](/images/Tools/LevelChanger/ColumnsLToSLB.png)
![ColumnsLToCLB](/images/Tools/LevelChanger/ColumnsLToCLB.png)
![ColumnsLToCAB](/images/Tools/LevelChanger/ColumnsLToCAB.png)
![ColumnsLToCBB](/images/Tools/LevelChanger/ColumnsLToCBB.png)
![ColumnsLToOAB](/images/Tools/LevelChanger/ColumnsLToOAB.png)
![ColumnsLToOBB](/images/Tools/LevelChanger/ColumnsLToOBB.png)

#### Top
![ColumnsLToSLT](/images/Tools/LevelChanger/ColumnsLToSLT.png)
![ColumnsLToCLT](/images/Tools/LevelChanger/ColumnsLToCLT.png)
![ColumnsLToCAT](/images/Tools/LevelChanger/ColumnsLToCAT.png)
![ColumnsLToCBT](/images/Tools/LevelChanger/ColumnsLToCBT.png)
![ColumnsLToOAT](/images/Tools/LevelChanger/ColumnsLToOAT.png)
![ColumnsLToOBT](/images/Tools/LevelChanger/ColumnsLToOBT.png)

Works on architectural and structural columns. 

### Experimental! Various With Two References

#### Bottom
![VariousLToSLB](/images/Tools/LevelChanger/VariousLToSLB.png)
![VariousLToCLB](/images/Tools/LevelChanger/VariousLToCLB.png)
![VariousLToCAB](/images/Tools/LevelChanger/VariousLToCAB.png)
![VariousLToCBB](/images/Tools/LevelChanger/VariousLToCBB.png)
![VariousLToOAB](/images/Tools/LevelChanger/VariousLToOAB.png)
![VariousLToOBB](/images/Tools/LevelChanger/VariousLToOBB.png)

#### Top
![VariousLToSLT](/images/Tools/LevelChanger/VariousLToSLT.png)
![VariousLToCLT](/images/Tools/LevelChanger/VariousLToCLT.png)
![VariousLToCAT](/images/Tools/LevelChanger/VariousLToCAT.png)
![VariousLToCBT](/images/Tools/LevelChanger/VariousLToCBT.png)
![VariousLToOAT](/images/Tools/LevelChanger/VariousLToOAT.png)
![VariousLToOBT](/images/Tools/LevelChanger/VariousLToOBT.png)

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

![MainTab](/images/Tools/LevelChanger/LevelChangerTabOther.png)

### Doors  

![DoorsLToSL](/images/Tools/LevelChanger/DoorsLToSL.png)
![DoorsLToCL](/images/Tools/LevelChanger/DoorsLToCL.png)
![DoorsLToCA](/images/Tools/LevelChanger/DoorsLToCA.png)
![DoorsLToCB](/images/Tools/LevelChanger/DoorsLToCB.png)
![DoorsLToOA](/images/Tools/LevelChanger/DoorsLToOA.png)
![DoorsLToOB](/images/Tools/LevelChanger/DoorsLToOB.png)

Works on standard door families hosted on the walls. 

### Windows  

![WindowsLToSL](/images/Tools/LevelChanger/WindowsLToSL.png)
![WindowsLToCL](/images/Tools/LevelChanger/WindowsLToCL.png)
![WindowsLToCA](/images/Tools/LevelChanger/WindowsLToCA.png)
![WindowsLToCB](/images/Tools/LevelChanger/WindowsLToCB.png)
![WindowsLToOA](/images/Tools/LevelChanger/WindowsLToOA.png)
![WindowsLToOB](/images/Tools/LevelChanger/WindowsLToOB.png)

Works on standard window families hosted on the walls. 

### Experimental! Curtain Doors  
  
![CDoorsLToSL](/images/Tools/LevelChanger/CDoorsLToSL.png)
![CDoorsLToCL](/images/Tools/LevelChanger/CDoorsLToCL.png)
![CDoorsLToCA](/images/Tools/LevelChanger/CDoorsLToCA.png)
![CDoorsLToCB](/images/Tools/LevelChanger/CDoorsLToCB.png)
![CDoorsLToOA](/images/Tools/LevelChanger/CDoorsLToOA.png)
![CDoorsLToOB](/images/Tools/LevelChanger/CDoorsLToOB.png)

It is an experimental option. 

Did you know that Revit API allows you to change the level of curtain panel doors? It is a highly experimental option, so use it wisely. One thing to keep in mind is that editing curtain wall sometimes overwrites these settings back to default ones (base of curtain wall).

### Experimental! Curtain Windows  
  
![CWindowsLToSL](/images/Tools/LevelChanger/CWindowsLToSL.png)
![CWindowsLToCL](/images/Tools/LevelChanger/CWindowsLToCL.png)
![CWindowsLToCA](/images/Tools/LevelChanger/CWindowsLToCA.png)
![CWindowsLToCB](/images/Tools/LevelChanger/CWindowsLToCB.png)
![CWindowsLToOA](/images/Tools/LevelChanger/CWindowsLToOA.png)
![CWindowsLToOB](/images/Tools/LevelChanger/CWindowsLToOB.png)

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


