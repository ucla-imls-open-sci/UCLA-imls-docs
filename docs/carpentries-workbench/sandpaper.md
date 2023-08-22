---
title: Into Sandpaper
layout: home
parent: Carpentries Workbench
---

## What is Sandpaper?

Sandpaper is the an R Studio package that is used in the Carpentries Workbench. It is used to run, preview, and build Lessons locally.
It comes with a suite of commands that help you build, preview, and run the site. You can preview these commands in the R Studio Console by 
typing out "sandpaper::" . A list of commands should appear after the "::" . Below we will document and describe several key commands. 
Each command also has a short description that you can read.
![R Studio Console Accepts Sandpaper Commands]({{ site.basurl }}/assets/img/workbench/sandpaper_console.png)

### sandpaper::create_lesson()

This command in R Studio will create an empty Carpentries Workbench in the path provided in its argument. This is a good message to use in R Studio
if you want to create a new lesson using the Workbench. An example would be *sandpaper::create_lesson("/filepath/Carpentries Guide")*. This command
would create a new workbench with the name **Carpentries Guide** in the path you specified.



### sandpaper::draft_episode_md()

This command takes in 3 input









### sandpaper::serve()

Sandpaper::serve() is a command that will build and display your site in the bottom-right viewer of R Studio. (Tip: You can pop this view out
into it's own window) This command will incrementally update your Lesson as you make any changes. It is great for viewing changes in a quick manner
without having to constantly running sandpaper::build_lesson() or other build commands.