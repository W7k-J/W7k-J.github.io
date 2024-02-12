---
layout: post  
title: Revit API Experiments - 3d View Rotator
date: 2024-02-09 12:00:00
author: Julian
---
![PostPage](/images/2024_BlogPost/Rotator_MainPage.jpg)


<!--excerpt-->

There is an inside joke in BIM community in Poland, that we spend most of our time simply rotating the model. I decided to check if I can automate this part of being a BIM Coordinator 😉

<div>
  <div style="position:relative;padding-top:56.25%;">
    <iframe src="https://www.youtube.com/embed/sCTdD1Qohmc?si=FwOFek8hRoGw0228" frameborder="0" allowfullscreen
      style="position:absolute;top:0;left:0;width:100%;height:100%;"></iframe>
  </div>
</div>


```csharp 

Autodesk.Revit.ApplicationServices.Application app = commandData.Application.Application;
Autodesk.Revit.DB.Document doc = commandData.Application.ActiveUIDocument.Document;
UIDocument uidoc = new UIDocument(doc);

Autodesk.Revit.DB.View3D view3d = doc.ActiveView as View3D;

for (int i = 0; i < 1000; i++)
{
    ViewOrientation3D orientation = view3d.GetOrientation();

    XYZ eyePosition = orientation.EyePosition;
    XYZ upDirection = orientation.UpDirection;
    XYZ direction = orientation.ForwardDirection;

    Line testLine = Line.CreateBound(upDirection, direction);
    Line testLine2 = Line.CreateBound(new XYZ(0,0,0), eyePosition);

    XYZ p2 = new XYZ(0, 0, 15);

    double degree = 0.0174533 / 3;

    Line newLine = testLine.CreateTransformed(Transform.CreateRotation(p2, degree)) as Line;
    Line newLine2 = testLine2.CreateTransformed(Transform.CreateRotation(p2, degree)) as Line;
    //TODO: Learn more about Vectors 

    ViewOrientation3D newOrientation = new ViewOrientation3D(newLine2.GetEndPoint(1), newLine.GetEndPoint(0), newLine.GetEndPoint(1));

    view3d.SetOrientation(newOrientation);

    System.Threading.Thread.Sleep(2);

    uidoc.RefreshActiveView();
}

return Result.Succeeded;

```
