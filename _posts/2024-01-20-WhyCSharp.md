---
layout: post  
title: Programming for AEC - Why you should use C# in Revit?
date: 2023-12-26 12:00:00
author: Julian
---
![PostPage](/images/2024_1_Code_WhyCSharp/WhyCSharp.jpg)

<!--excerpt-->

[Collected on Linkedin:](https://www.linkedin.com/feed/update/urn:li:activity:7150609562478223360/?commentUrn=urn%3Ali%3Acomment%3A%28activity%3A7150609562478223360%2C7150789086658609152%29&dashCommentUrn=urn%3Ali%3Afsd_comment%3A%287150789086658609152%2Curn%3Ali%3Aactivity%3A7150609562478223360%29&dashReplyUrn=urn%3Ali%3Afsd_comment%3A%287154480446024626176%2Curn%3Ali%3Aactivity%3A7150609562478223360%29&replyUrn=urn%3Ali%3Acomment%3A%28activity%3A7150609562478223360%2C7154480446024626176%29)  

Please find below some valid points from a discussion about superiority of using C# in Revit (building Add-ins, using Dynamo):

Some points from me: 
1. It is not harder than Python – C# is a very modern high-level language. Even as C# 7 used in current in Revit Net Framework it is clear and easy to learn. After coming from Python, you might encounter some annoying things like slicing the lists, but who cares. Personally, I prefer LINQ to Python's list comprehension (BTW I haven’t seen it used much in Python code for Revit API).
2. It is not hard to set up the environment for it – It takes 25 minutes to do it. After that you are good to go and will not have to do it again for a long time. For simple things you can start with Revit Macros and it will take you even less time. 
3. C# is statically typed language. It is forcing you (not very strongly, you can use var) to know what exactly you are doing. I found it extremely helpful while learning Revit API (and programming in general). 
4. It is used by the best programmers in the AEC industry. Sorry but a lot of Python code available online is over commented, overcomplicated rubbish. It works, but if you need a comment every second line there is something wrong with it.
5. Use of your own classes, as others already mentioned. To it, I will add extensions methods - they are so good!

A very valid point from [Fernando Borges](https://www.linkedin.com/in/fernandoaugustoborges/):

6 - almost every (good) software running on Windows platform exposes it's functionality as a .NET API. It's just simple as referencing a .dll inside your project to make it accessible from inside you Revit Plug-in. 

Please contact me if you would like to add some other points! 