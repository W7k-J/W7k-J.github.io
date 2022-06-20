---
layout: post  
title: Dynamo Script - Assign Room Names To The Ceilings Above
date: 2022-06-18 12:00:00
author: Julian
---
![PostPage](/images/Dynamo/DS1/20220618_Logo.png)

<!--excerpt-->

I’ve recently started using dynamo again more often which made me spend some time playing with it.   
Today I ended up doing some learning material from <http://learndynamo.com/>  

The whole course is super cool and long time ago I used this script to solve a big task. It is allowing you to assign the number of the room below to the ceiling above. Cool thing often needed in Fit-Out projects.  

I decided to take a deeper look on it and play a little with it.  
Before continuing reading, please check Jeremy’s post about his script at: 
 
<http://learndynamo.com/mod1/>  

His explanations are great!  
  
So let’s go through the changes I did.
  
![Script with changes](/images/Dynamo/DS1/20220618_schemat.png)  
  
  
### Adding exception to Python Code (1)  
  
  
A lot of people in the comments didn’t know why sometimes the script was not working. The problem is that in case of not finding the room below the ceiling python doesn’t know what to do. So it crashes.  
Below is the solution to this problem (google: try and except in python). As you can see in case of not finding the room the script is adding “No Room” to the list instead. 


```python
if toggle == True:
	for point in points:
		try:
			room = doc.GetRoomAtPoint(point.ToXyz())
			lst.append(room.LookupParameter("Name").AsString())
		except:
			lst.append("No Room")

	OUT = lst
```
  
  
### Filter out ceilings without rooms (3)
  
  
I decided to filter out the ceilings to which script is unable to assign proper room number. I didn’t want it to later overwrite ceilings which were manually corrected.
  
  
### Assign Room Name instead of Room Number (3)

That’s probably the biggest change requested by many in the comments. At the beginning I thought it should be quick change but apparently Iron Python has some problems with using room names.

You can access it by using .LookupParameter() and this is how I did it in the end. Of course you can also use dynamo to swich numbers into names - that was my first idea after having problems with "Room name".
 
  
### Parameter Name (4)
  
  
Revit parameters should not contain mathematical operators (+, -, /, ) in names so I changed it from “CEILING-ROOM’ to “Ceiling_Room”. The reason behind it is that later you can’t use them easily in formulas.
  
  
Please find the link to the script below:

[download](https://w7kpl-my.sharepoint.com/:u:/g/personal/jw_w7k_pl/EQOmeh7hRjdMnCuI5K_HqGoBPi9Ey0smVrYpMXlEvga7Aw?e=VtWC8C)

![Script highres](/images/Dynamo/DS1/20220618_AssignRoomToCeiling.png)
