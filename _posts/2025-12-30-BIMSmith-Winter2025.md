---
layout: post  
title: BIMsmith Winter Wonderland Holiday Revit Competition 2025 - Revit Game Freerider
date: 2025-12-30 12:00:00
author: Julian
thumbnail: /images/thumbs/2026_BlogPosts/RevitFreeRiderTitle.jpg
---
![PostPage](/images/2026_BlogPosts/RevitFreeRiderTitle.jpg)

<!--excerpt-->

As each year it is the time, when I want to share a short summary of what happened this year and, of course, my submission for #BIMsmithWinterWonderland organized by BIMsmith.

It’s been a good year! Architecturally, I continued working on projects in London while still staying active in Poland. At the same time, I managed to update almost all of my tools and even published a new one, Boxer. I also tackled some cool scripting challenges along the way, made some great UAV photos, took active part in 2 webinars…

But, back to the challenge… I decided to experiment a little and as always push the boundaries a little bit. Over the past few years, I’ve seen some amazing submissions featuring animated parts. It is something I (and a few others) helped to introduce to this challenge. Today, it’s almost standard for many submitted families to move, rotate, or perform other interesting actions.

But as much as animations are fun, they’re still static in nature. Typically, you use Dynamo to change parameters, export images, and later compile them into a video. That made me wonder: Could I make the family respond dynamically? Maybe even with a keyboard? Internet said that it might be super hard and problematic, so I decided to do it… 

Another goal was to test the limitations of Revit Macros. A few years ago, Autodesk gave us a big gift by ditching SharpDevelop and allowing us to use Visual Studio Code. In my opinion, it’s the best way to write and test code today, yet it hasn’t received enough attention from the Revit community.

The last part of my experiment involved using AI for coding. I’ve used it before, but this time I relied on it heavily - trusting it to create, update, and introduce new features continuously. My feelings are mixed: AI helped me finish the task quickly, but the code quality was poor. I had to double-check everything, and it made a lot of mistakes - reverting to previous already corrected versions without permission or calling methods that didn’t exist. Asking AI in the middle of night to “change this, but please don’t change the rest” wasn't funny. 
 
In the end, I built a 2D game where the user controls a ski freerider with three buttons (W, A, D): jump, move left, and move right. I ended up implementing a basic physics system for gravity, collision detection with Revit lines, and simple animations. I also added forms to inform users about the game and restart it. The skier family is simple but customizable (for example you can adjust its height and weight which affects macro), has some basic animations and it’s highly optimized to minimize processing, which happens almost every frame. The Revit interface is also not freezed which allows you to normally zoom in and out. 

It is probably the first family used for dynamic game in Revit! Feel free to use it in some of your details - The code will be available on my github account soon.

[Link to Github](https://github.com/W7k-J/W7k.RevitFreerider)!


So good luck in the new year! And happy skiing!

<div>
  <div style="position:relative;padding-top:56.25%;">
    <iframe src="https://www.youtube.com/embed/4wezThWK8SI?si=QsPTMZToYJi19Eva" frameborder="0" allowfullscreen
      style="position:absolute;top:0;left:0;width:100%;height:100%;"></iframe>
  </div>
</div>
