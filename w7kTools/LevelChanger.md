---
layout: toolspage
title: Level Changer
permalink: /tools/levelchanger
---

![MainTab](/images/Tools/LevelChanger/LevelChangerTab.png)

The purpose of this tool is to allow you to change reference levels without changing element's location / elevation. The tool is going to do it automatically. It will set correct offsets for you. 

No longer you will have to manually calculate them. Simply choose new level (or use other provided option ) and it will be done. Moreover because the tool changes the offsets and levels at the same time your Revit model will not explode in the process. 

## Options

![MainTab](/images/Tools/LevelChanger/LevelChangerExtendedOptions.png)

Each of the buttons has 6 different option you might use:

### Default  

You will be prompted to choose <b>one level</b> and the tool will try to set it for all selected elements:  
   
![MainTab](/images/Tools/LevelChanger/LevelChangerSelection.png)

### Set level to the Closest 

The tool will automatically choose <b>the closest level</b> (the one which will result in the smallest offset) for your elements and the tool will try to set it for all selected elements.  

The levels will be calculated separately for all selected elements.

### Set level to the Closest Above

Similarly, The tool will automatically choose the closest level for your elements, but this time it will look only for a level which elevation is above the selected elements. 
The levels will be calculated separately for all selected elements.

<i>For example  
if you have a floor between two levels the tool will always assign the level above your floor - even if the offset would be comparable larger then to level below. </i>


### Set level to the Closest Below

Similarly, The tool will automatically choose the closest level for your elements, but this time it will look only for a level which elevation is below the selected elements. 
The levels will be calculated separately for all selected elements.

<i>For example  
if you have a floor between two levels the tool will always assign the level below your floor - even if the offset would be comparable larger then to level above.</i>

### Set level to the one above currently selected 

The tool will automatically change the reference level to one above currently selected.
The levels will be calculated separately for all selected elements.

<i>For example  
if you have a floor on level 1 it will change its reference to level 2 and its offset to -3000 mm. </i>


### Set level to the one below currently selected 

The tool will automatically change the reference level to one above currently selected. 
The levels will be calculated separately for all selected elements.

<i>For example:  
if you have a floor on level 2 it will change its reference to level 1 and its offset to 3000 mm. </i>

## Levels - Objects With One Reference
![MainTab](/images/Tools/LevelChanger/LevelChangerTabOneRef.png)

Floors

Roofs 

Ceilings

Pads (for older versions of Revit (pre 2024))

Experimental! Various With One Reference

## Levels - Objects With Two References
![MainTab](/images/Tools/LevelChanger/LevelChangerTabTwoRef.png)

Walls 
  Top
  Bottom

Columns 
  Top
  Bottoms

Experimental! Various With Two References
  Top
  Bottoms

## Levels - Other Objects
![MainTab](/images/Tools/LevelChanger/LevelChangerTabOther.png)

Doors

Windows

Experimental! Courtain Doors

Experimental! Courtain Windows 

# Video

<div>
  <div style="position:relative;padding-top:56.25%;">
    <iframe src="https://www.youtube.com/embed/i5vvm8kygQ4" frameborder="0" allowfullscreen
      style="position:absolute;top:0;left:0;width:100%;height:100%;"></iframe>
  </div>
</div>
<br>
<br>
<div class="backToTools">
    <a href="https://w7k.pl/tools/">Go Back to tools</a>
</div>
<br>
<br>
<div class="terms">
    <a href="https://w7k.pl/terms/">Disclaimers, Policies, Terms & Conditions</a>
</div>