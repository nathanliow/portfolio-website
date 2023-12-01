---
title: "youmecar"
description: "A ride sharing web application that facilitates event organization 
for different organizing entities from clubs to church groups."
heroImage: "/projects/youmecar/hero.png"
pubDate: "Oct 1 2023"
badge: "IN PROGRESS"
tags: ["Python", "React", "Firebase"]
code: ""
demo: ""
blog: ""
---
# Overview #
A ride sharing web application that facilitates event organization for different
organizing entities from clubs to church groups.

# Purpose #
This application aims to facilitate ride organization within a community so people
without cars (riders) can be easily sorted into groups with a driver. It serves a 
large number of people unlike an individual using Uber or Lyft and serves a middle
ground between close friends organizing a trip and complete strangers getting on a bus
together. 

Some common and practical applications of this web-app can be within school organizations,
church groups, one-time events, and field trips.

# How it was made #
<br/>
<center>
    <img src="/projects/youmecar/initial.png" alt="The initial figma idea" width="400" height="200">
    <p class="caption">The initial figma idea I had in mind, months before HackTX 2023</p>
</center>

I was inspired by the idea of creating an automatic ride-sheet when the church I went to
used Google Sheets every week to organize who will go into what car. I found this to be
quite tedious and knew it must've been a lot of work for the organizers as well, especially
if there was more than one event going on, all of which requiring a separate ride sheet. The
idea never had the chance to leave the microcosm of my mind due to the busyness of school
but I knew I wanted to do something about it.

<br/>
<center>
    <img src="/projects/youmecar/board.png" alt="Drawing board of app flow" width="400" height="200">
    <p class="caption">The drawing board of our app's flow</p>
</center>

The opportunity finally arose when HackTX 2023 rolled around and I proposed this idea to my
team for the hackathon. This event jumpstarted work on the project and we spent the next 16
hours designing, drawing, and creating the frontend as well as the backend of the web app.
We first drew out how the pages were going to look like on Figma, then we began routing the
different pages within a new React app. After getting some basic form input boxes in their 
necessary pages, we started styling the pages using Tailwind and linking them together. 
We also integrated Firebase for database storage to store the logins of users and what 
organizations, events, and cars they were in. 

<br/>
<center>
    <img src="/projects/youmecar/role.png" alt="Role selection page" width="400" height="200">
    <p class="caption">The role selection page</p>
</center>

That was as far as we were able to go within the length of the Hackathon but we slowly 
continued working on the project. Continuing to style the pages to look like our Figma
drawings and linking the frontend and the backend to make the web application more 
responsive and interactive.

Currently, we are still working on linking the frontend and backend to work towards a 
minimum viable product (MVP) so that we can let users test it and we can move onto the 
polishing stage.

# Challenges #
1. &nbsp;&nbsp;&nbsp;&nbsp;1\. Styling the frontend
2. &nbsp;&nbsp;&nbsp;&nbsp;2\. Linking the backend with the frontend

This project had by far the most difficulties that I personally encountered. The first of
which was learning TailwindCSS and styling the frontend. It had been a while since I had 
used HTML, CSS, and JavaScript so getting the behavior and appeal I was looking for was a
tedious and iterative process. Understanding the syntax of Tailwind took some time to get
right as well.

Another challenging aspect of this project was the integrating of both the frontend and the
backend to create a full-stack web application. There was a lot to learn with how Firebase
works and encountering a lot of new concepts with databases and transferring data didn't 
ease the challenge. Even now, I'm still trying to figure out how I can store the car that
a user is selected in and what the best solution to that problem might be as a user can be
in dozens of cars at the same time. Then the bigger problem is how we collect all that data
to show a user every seat that is taken by other users so that the capacity of cars can be filled.
Another idea that we were hoping to implement on the backend using Python was the ability to
sort incoming people into cars if they so choose, without needing to click on a certain car if
they didn't have a preference for a driver. We also wanted to implement a party system so that
one person can sign up a group a people.

The overarching goal and barrier to this project is: **how can we make this better and easier than
a Google Sheet.** After all, that is what we are trying to replace and automate. That is the vision
our team is trying to hold as we work towards an MVP and eventually a polsihed product for practical
use. 

# Impact #
The vision for the impact of this web application traces back to where the idea was inspired. Within my
own local communities, I hope this application can automate some of the tasks currently held by one person 
and I hope it makes it less tedious for riders to sign up for recurring events every week. This would
ultimately save a lot of time and resources for those involved with organizing such events. 

Zooming out a little bit, I hope this application can find its use within college organizations such as clubs
or even volunteer groups who may need a ride-sheet system to go to local food banks or high schools to do
their work. Beyond that, it may find its use case with one-off parties to a club, bowling alley, arcade, or
hiking trail.  

I believe the possibilities of its use-cases are endless as there doesn't seem to be an obvious company
that current fills in this gap. I also believe the impact of this application can reach far beyond my
own communities and facilitate the organization of events for many different communities.

# Full Tech Stack #  
| Frameworks | Languages    | Libraries     | Tools      |
| :--------- | :----------- | :------------ | :--------- |
| - React    | - Python     | - TailwindCSS | - Firebase |
|            | - HTML       |               | - VSCode   |
|            | - CSS        |               |            |
|            | - JavaScript |               |            |
