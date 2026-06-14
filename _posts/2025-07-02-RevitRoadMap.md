---
layout: post  
title: How did I end up coding another tool from Revit Roadmap? 
date: 2025-07-02 12:00:00
author: Julian
thumbnail: /images/thumbs/2025_BlogPost/StairsFromAutodeskRoadMap.jpg
---
![PostPage](/images/2025_BlogPost/StairsFromAutodeskRoadMap.jpg)

<!--excerpt-->

How did I end up coding another tool from Revit Roadmap?
  
I’m not going to lie - as my programming skills grow, my tolerance for mindless clicking is dropping fast. It’s time-consuming, error-prone, and slowly takes away the joy of being an architect.
  
So, when I heard we needed to check over 200 drawings to ensure stair paths were added to every single stair… I knew I had to automate it.
  
In general, there were some challenges I had to solve:
  
1. Finding stairs in linked files (Revit 2020–2023): The API doesn’t make this easy - I had to get creative. So, I ended up converting stairs and view crop boxes to bounding boxes to check if they intersect - Why was I reading fantasy books at school during math classes?  
2. Handling existing stair paths: Avoiding those annoying duplicate errors was a challenge. Plus, I learn that Revit is not good in finding them for the links. In the end “Try and catch” was my big friend - not my general approach, but it worked.  
3. Improving the selection experience: I tweaked my selection class to make the tool more user-friendly.
  
Not sure if that’s the best long-term approach, so I’d love to hear your thoughts. I’m considering building a more robust tool that handles both cases across all views, with options to include/exclude links.
  
While digging through internet and some forgotten parts of Autodesk Forum to find some info about some hashtag#RevitAPI classes, I stumbled on a post by Kimberly Fuhrman-Jones, Assoc. AIA - it turns out this exact feature is now on the Autodesk Revit Roadmap. (Revit Products Forums/Revit Ideas/Tag All Untagged - Stair Path Arrows)
  
Still, I’m adding this one to my personal collection of “scripts I built before Autodesk did.” Bonus: mine works in Revit 2020-2026. Not bad for an architect. 😊
  
Video below:  

<div>
  <div style="position:relative;padding-top:56.25%;">
    <iframe src="https://www.youtube.com/embed/Hy5fSEXGBnI?si=V2bn0NkVK2yGazRQ" frameborder="0" allowfullscreen
      style="position:absolute;top:0;left:0;width:100%;height:100%;"></iframe>
  </div>
</div>
