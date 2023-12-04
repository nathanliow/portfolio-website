---
title: "Physics Calculator Website"
description: "A website that assists calculations for physics-related topics such as kinematics, 
projectile motion in 2D space, and collisions."
heroImage: "/projects/physics-calc/hero.png"
pubDate: "April 1 2023"
badge: ""
tags: ["Python", "HTML", "JavaScript"]
code: ""
demo: "https://liowapps.pythonanywhere.com/"
blog: ""
---
_Note: pythonanywhere.com only supports website hosting for 3 months at a time so the
demo may not be live at all times._  
_Last reloaded: December 1st, 2023_  
_Live until: March 1st, 2024_  

# Overview #
A website that assists calculations for physics-related topics such as kinematics, 
projectile motion in 2D space, and collisions. 

It also includes an unfinished portfolio tracker that only returns the price of certain coins. 

# Purpose #
This website was made to apply my understanding of physics as well as further my
knowledge of Python. It also gave me a chance to work with some HTML and Flask as I
deployed the website. The bigger plan was to allow others to also visit and use the 
website to assist in their own physics calculations.

# How it was made #
As I was starting this project, I didn't think it would be too difficult as it
would simply just automate certain formulas and calculations. But as I began work,
I had to draw out the functionalities of the calculator and quickly realized the 
different combinations of how input could be gathered. Given so many variables, I
had to work out which ones and how many of them were to be used to calculate the 
desired answer. For example, I wrote out and calculated the formulas to solve for each
individual variable for the kinematic equations to account for the different combinations
of input. In hindsight, I believe this process could've been much easier and more efficient.

The majority of the code was written in PyCharm and tested on the terminal. Then I searched 
for ways to create a simple frontend for my code so that a user didn't have to interact with 
the terminal. This is where I stumbled upon 
<a target="_blank" href="https://www.pythonanywhere.com/">pythonanywhere.com</a> which allowed
me to host my Python scripts for free while adding easy-to-use website templating. After some
time creating input boxes and integrating my code, the website went live.

This project had been one of my firsts and I believe the organization of the code as well as 
the solution approach to solving the problem reflects that. Looking back, it has shown me 
clearly how much I've learned and improved since working on this project.

# Challenges #
1. &nbsp;&nbsp;&nbsp;&nbsp;1\. Integrating Python code into a frontend
2. &nbsp;&nbsp;&nbsp;&nbsp;2\. Testing and ensuring accurate answers

The hardest challenge about this project was integrating my code into pythonanywhere.com's
structure. I had to convert my code from taking input from the terminal to taking input
from forms on a website. This was especially hard as this was when I had no prior experience
with frontend and no knowledge of how HTML or JavaScript works. This process took a lot of trial
and error to get right.

Another minor difficulty with this project was my ability to fully test out the code. This would
include logical errors where the calculator would simply be wrong, or the calculator would
provide an answer to a physically impossible scenario. Many of these bugs were hard to catch and
find as the number of scenarios that could be inputted into the calculator was endless. Mathmatically, 
the numbers would work out, but conceptually it was all nonsense. I accounted for this by adding 
some checks in the code to ensure that the scenario was physically possible to begin and testing 
every type of number I could have possibly inputted.

# Full Tech Stack #  
| Frameworks | Languages    | Libraries | Tools                |
| :--------- | :----------- | :-------- | :------------------- |
| - Flask    | - Python     | - numpy   | - pythonanywhere.com |
|            | - HTML       |           | - PyCharm            |
|            | - JavaScript |           |                      |
|            |              |           |                      |
