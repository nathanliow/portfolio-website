---
title: "Manim Animation"
description: "A 3D animation of Ampere's Law as learned in my AP Physics C: Electricity and Magnetism class. 
It uses a Python library called Manim (short for Math Animation), created by Grant Sanderson, which enables
the rendering of complex scenes to model practically any math-related concept."
heroImage: "/projects/manim/hero.png"
pubDate: "April 24 2023"
badge: ""
tags: ["Python", "Manim", "Video Animation"]
code: "https://github.com/nathanliow/Physics-with-Manim"
demo: "https://youtu.be/7Fo4dofZfcc"
blog: ""
---
# Overview #
A 3D animation of Ampere's Law as learned in my AP Physics C: Electricity and Magnetism class.
It uses a Python library called Manim (short for Math Animation), created by 
<a target="_blank" href="https://twitter.com/3blue1brown">Grant Sanderson</a>, which enables
the rendering of complex scenes to model practically any math-related concept.

# Purpose #
I was inspired by the animations created by Grant on his 
<a target="_blank" href="https://www.youtube.com/@3blue1brown">youtube channel</a> and I wanted to
further my understanding of Python. I was also working on graphic organizers for my AP Physics 
class and figured this project would be a good complement to the whole physics-themed ecosystem
I had been creating. 

# How it was made #
I first needed to learn the syntax and concepts within Manim which required some time reading the 
<a target="_blank" href="https://docs.manim.community/en/stable/">documentation</a>. The library
uses math objects or "mobjects" as building blocks to create more complex structures. Mobjects
can be shapes and graphs which can be transformed, translated, and customized.  

After grasping some fundamentals of Manim, I began with a storyboard with what I wanted to show on
the screen, from the formulas to the orientation of how I envisioned my animation would progress. 
I aimed to create the perfect tutorial I had formulated in my head, something I wish I could have watched 
that would have instantly explained the physics concept to me. After getting a general guideline to follow
I started creating individual scenes. 

I began making the mobjects and moved the individual pieces into position. This quickly became a long and
tedious process as it was difficult to pinpoint the right positions for the mobjects to get the look I
was looking for. After following the the storyboard I had made and adding some extra implementation details,
I continued to expand the number of scenes I wanted to animate, in an attempt to make the explanation
flow simply and naturally.

Once I was satisfied with the animations, I integrated a text-to-speech voiceover and finally used Windows
Clipchamp to edit the scenes together to the final product.

# Challenges #
1. &nbsp;&nbsp;&nbsp;&nbsp;1\. Making everything 3D
2. &nbsp;&nbsp;&nbsp;&nbsp;2\. Placing mobjects and text in the right places
3. &nbsp;&nbsp;&nbsp;&nbsp;3\. Long rendering times

The biggest challenge of this project was creating in a three dimensional space. The introduction of depth
meant mobjects had to be layered on top of each other as well as positioned right next to each other in
three different axes. When I finally get two mobjects to fit nicely together, my hopes would come crumbling down
as I move the camera and see the mobjects completely disjointed from each other. This became a long and 
tedious process of trial and error at the pixel level to get the results I needed.

Another difficulty I faced that came along the nature of three dimensional space was the placing of 
inherently two dimensional mobjects such as dots, lines, and text. This meant I had to specifically 
place mobjects at an angle so that it would be legible and appealing. This again took dozens of trials
just to get right.

One new challenge I encountered working with animation specifically was the rendering times, specifically with
Manim. Being a Python library, it had limitations when it came to accessing my computer's resources so the 
rendering times were capped with no way to workaround it. 8 second scenes would take about 45 seconds to 
fully render with marginal improvement when rendered at a lower quality but the amount of time would stack
up quickly as I rendered the animations as a way to check my work. Rather than test cases to pass, I had to
rerender the scene to see if my one changed line of code had the effect I was looking for. This challenge was
mitigated as I learned to section off my scenes so that the program didn't have to rerender every single 
scene I had made.

# Impact #
I ended up presenting this video animation to my high school physics teacher who found my dedication and
effort admirable. He said he planned to use my work (and Physics Grahpic Organizers) as an additional tool 
and resource to help future AP Physics students learn the concepts in the notoriously difficult subject. 
I'm hoping this video would help at least one person understand the niche subject of Ampere's Law, but 
maybe more so to be inspired. 

# Full Tech Stack #  
|  | Languages | Libraries | Tools       |
| :--------- | :-------- | :-------- | :---------- |
|            | - Python  | - Manim   | - Clipchamp |
|            |           |           | - VSCode    |
|            |           |           |             |
|            |           |           |             |