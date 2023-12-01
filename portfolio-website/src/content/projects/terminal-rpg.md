---
title: "Codecademy Terminal RPG"
description: "A role-playing game (RPG) that's played on the terminal."
heroImage: "/projects/terminal-rpg/hero.png"
pubDate: "June 1 2023"
badge: ""
tags: ["Python"]
code: "https://github.com/nathanliow/Codecademy-Terminal-Project"
demo: ""
blog: ""
---
# Overview #
A role-playing game (RPG) that's played on the terminal. This project was done as part of a 
<a target="_blank" href="https://www.codecademy.com/career-journey/computer-science" download>
Python Computer Science</a> career path at Codecademy.com. This was taken in preparation over 
the summer for my data structures class. 

# Purpose #
This project helped me grasp object oriented programming as well as encapsulation and multi-class
structured programming. It also honed my Python skills and knowledge. Additionally, this project 
required me to learn Git and version control which are both extremely useful skills I still use 
to this day.

# How it was made # 
A general guideline is given on the codecademy website help brainstorm ideas for projects. I 
used this to formulate what I wanted to build. I took inspiration from games I had played
when I was younger and decided to make an adventure-type game. I first began with a main 
program but as it quickly expanded, I realized I needed to organize the elements of my 
program in different files. This was done by separating my game into the environments 
that my player would traverse through and the enemies that the player would face. After some 
integration of different features like an inventory and trading system, there was only
some polishing required in the end.

# Challenges #
1. &nbsp;&nbsp;&nbsp;&nbsp;1\. Trading and inventory system
2. &nbsp;&nbsp;&nbsp;&nbsp;2\. Learning Git and using GitHub

A major challenge I encountered while building out my program was implementing the trading
and inventory system I had envisioned. At the time, I wasn't sure what the best way to allow
the player, villagers, and enemies to possess items. I also wasn't sure how to uniquely 
identify or classify an item. For example, I didn't know whether there could be duplicates
of the same level 5 common sword. In the end, I allowed duplicates and created a class to
create instances of Item objects to represent an individual item. Then these items were
possessed by entities within their inventories which were internally native arrays. This
design seemed to work quite well while allowing the flexibility to have any number of any
item.

Another challenge that came with the project was the need to learn Git. Before I had
discovered GitHub Desktop, I manually typed in all the terminal commands to add my 
changes to the staging area and commit them to its respective repository. However,
I believe using the "more primitive" and slower in the beginning helped me fully understand
what the purpose of Git was and how it fully worked. 

# Full Tech Stack #  
|            | Languages |           | Tools        |
| :--------- | :-------- | :-------- | :----------- |
|            | - Python  |           | - VSCode     |
|            |           |           | - Codecademy |
|            |           |           | - Git        |
|            |           |           |              |