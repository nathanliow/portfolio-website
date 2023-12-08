---
title: "Creating my Portfolio Website"
description: "An attempt to learn all about a completely new language and 
to simply throw myself into the deepend. Definitely encountered many 
struggles but determination has brought me far."
pubDate: "Nov 27 2023"
heroImage: "/blogs/post1/hero.png"
badge: ""
tags: ["Astro", "Portfolio Website"]
updatedDate: "Nov 28 2023"
---
# How it began #
I wanted to create something that was personal and uniquely mine. It also felt like I had finally 
enough projects to display for the world to see. It was like a weird attachment to the idea of 
owning a little corner of the internet. For every internship I applied to, I would simply skip 
over the "personal website" text box entry, but I always felt a little sting for not having 
something to place in there. I wanted to change that, while getting an easy opportuntity to 
learn something new. 

# The journey of how was it made #
I told some friends about the idea of making a personal portfolio website 
using React as that was the extent of my frontend knowledge but they were 
quick to tell me that wasn't necessary. What I needed was a static website 
generator. The idea seemed obvious enough, a portfolio website was a static 
website kind of idea. I looked into different static site generators and came 
across this <a target="_blank" href="https://jamstack.org/generators/">Jamstack</a>. 
A little scrolling later and I settled on using Astro. 

So why Astro?

Aside from a personal referral, the 
<a target="_blank" href="https://docs.astro.build/en/getting-started/">extensive documentation</a> 
made it very beginner friendly, especially with my limited JavaScript knowledge at the time. 
Astro also makes the website blazing fast by stripping JavaScript and unused elements. 
The various integrations Astro supports will allow me to scale in the future, not 
just with this website but with future websites I may create. Astro just came with everything 
I needed, along with being easy to use and straight to the point. As someone who knew nothing 
about frontend, I'd recommend giving Astro a try. 

<br/>
<center>
    <img src="/blogs/post1/figma.png" alt="Website design on Figma" width="400" height="200" class="blog-img">
    <p class="caption">Designing the website on Figma</p>
</center>  

The process of building the website began with designing my website on Figma. Then it went to 
hours of reading Astro documentation and understanding how to use Astro in my project. I started
building my first Astro component, which was the Content Box that houses the information of a 
blog or project. This consisted of a picture, a title, a description, a badge, and a group of tags. It took some time to create and piece together smaller components that I realized I had to make such
as each individual tag but the Content Box component wasn't much trouble.  

From there, I moved onto making the Sidebar which took many more hours of styling and adjusting to get right. It was at this point I had discovered daisyUI to help make the drawer sidebar which made life a bit easier. Then I went to styling entire pages and smaller components such as the Navigation
Bar. I integrated some color and text as well as gradients to spice up the website a little.

After some polishing, I began writing documentation for the past projects that I wanted to feature
on the website and now, the website has been published on to Netlify for the world to see.

# Some challenges about this project #
Some of the hardest challenges of this project:
1. &nbsp;&nbsp;&nbsp;&nbsp;1\. Making resizing natural so it flows and works smoothly on all devices.
2. &nbsp;&nbsp;&nbsp;&nbsp;2\. Maintaining a consistent and natural project structure. 
3. &nbsp;&nbsp;&nbsp;&nbsp;3\. Learning all the different tools necessary for creating a portfolio website.  

<br/>
<center>
    <img src="/blogs/post1/resize.png" alt="Resizing being a pain" width="200" height="100" class="blog-img">
    <p class="caption">The sidebar failing to be a sidebar on phone screen sizes</p>
</center>

Resizing was by far the most difficult part to get right when building the website. It was only a 
problem I noticed about halfway into development. I noticed that for smaller screen sizes such as 
phones, the sidebar would not scale all the way down, leaving an awkward rectangle on the top half 
of the screen. The color of the background would also not fit the entire screen at certain widths 
and the scrollbar would popup inconsistently. All these different issues left me confused for hours 
on end. I first tackled the background so that the color would fill the entire screen which required 
styling the broader div container to have the same background color. In order to fix the inconsistent
scrollbar, I revamped my width and height structure of all of the image and text content present on 
the screen so that it would always have max width between the borders of the viewing window. This one 
took a bit but I had eventually the right settings to make it flow seamlessly. Then came the sidebar, 
which took days to configure and dozens of iterations to ensure it would pull out right, have the 
buttons scaled and stay in its consistent position, style the text to give it some personality, 
and have it all not break when the screen became smaller. 

Another problem I faced when diving into frontend with having minimal prior knowledge was the unspoken 
and untaught knowledge of having a neat and organized project structure. Knowing where to place files 
and where to install packages was a headache to get right as it was difficult to find an answer when 
my project was unqiue and so was everyone else's. Things quickly got cluttered and messy and moving 
files between folders became painful when the imports and components are all linked together. It took 
some time before the directories became natural and I could quickly naviagate through the project.

<br/>
<center>
    <img src="/blogs/post1/structure.png" alt="Organized" width="200" height="1000" class="blog-img">
    <p class="caption">Satisfying organization of files for this project</p>
</center>

Despite the excellent documentation provided by some of the tools I used, I still struggled to 
understand the necessity for some lines of code or the purpose of certain elements in a design. 
Using tools like Figma, daisyUI, Astro, or just basic HTML, JavaScript, and CSS, I would sometimes 
find myself roadblocked by alien syntax and keywords. These roadblocks led to hours of processing 
and studying documentation in order to understand what the code I'm looking at is trying to do. 
For example, learning all the different keywords of CSS and JavaScript in order to achieve the look 
and behavior I'm going for took many iterations to get just right. Or the way how variables are 
passed down through different components and how files are linked also created a steep learning 
curve I had to conquer. 

# Conclusion #  
In the end, I'm proud of what I was able to build in about a week. I believe I gained a solid 
fundamental understanding in for Astro, daisyUI, and even Markdown while also furthering my 
understanding in HTML, CSS, and JavaScript. I think this knowledge will definitely help in 
future frontends I may embark on and I'm excited for what I may build in the future. For now, 
there's still a lot to learn and discover.

# More resources I found helpful for this project #
1. &nbsp;&nbsp;&nbsp;&nbsp;- <a target="_blank" href="https://css-tricks.com/css-link-hover-effects/">CSS Hover Tricks</a>
2. &nbsp;&nbsp;&nbsp;&nbsp;- <a target="_blank" href="https://daisyui.com/">daisyUI Documentation</a>
3. &nbsp;&nbsp;&nbsp;&nbsp;- <a target="_blank" href="https://www.markdownguide.org/basic-syntax/#escaping-characters">Markdown Guide</a>
4. &nbsp;&nbsp;&nbsp;&nbsp;- <a target="_blank" href="https://astro.build/themes/">Astro Themes</a>