---
layout: post  
title: Revit API Experiments - TemporaryGraphicsManager
date: 2024-02-16 12:00:00
author: Julian
---
![PostPage](/images/2024_BlogPost/TemporaryGraphicsManager.jpg)

<!--excerpt-->

Today, I would like to share a recent discovery I made while working with Revit API. As many of you know, creating new graphical elements within Revit can be quite challenging and limited. However, I stumbled upon a little-known class called TemporaryGraphicsManager.

The TemporaryGraphicsManager allows us to add temporary graphical elements directly to the model or drawing space. These graphics are not subject to undo actions and are not permanently saved anywhere. While they won’t clutter up your project, they provide a powerful way to enhance your user experience.

Surprisingly, I haven’t seen this class widely used in other plugins or extensions. So, when I first encountered it, I knew I had to put it to the test. 
In the initial part of my video, I demonstrate how to align title lines to previously saved points. With a simple click, you can create temporary graphics that will guide your design process and allow you to snap your title lines to them! 

In the second part of the video, I collect points and save them to an external file for future reference. The TemporaryGraphicsManager conveniently marks their locations, eliminating the need to remember which points I’ve already saved.

Is this the easiest method of controlling title lines? Perhaps not. In an upcoming update to my Drafter tool, I’ll introduce further automations in this area. But one thing is certain: I’ll continue to leverage the power of TemporaryGraphicsManage.

<div>
  <div style="position:relative;padding-top:56.25%;">
    <iframe src="https://www.youtube.com/embed/Q7aKEocvRtk?si=Y5OectK0apKbNwcK" frameborder="0" allowfullscreen
      style="position:absolute;top:0;left:0;width:100%;height:100%;"></iframe>
  </div>
</div>

As requested I also saved some info about my points :

[Values](/images/2024_BlogPost/TemporaryGraphicsManagerPoint.jpg)

[MyPoint](/images/2024_BlogPost/point.bmp)

