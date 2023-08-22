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
if you want to create a new lesson using the Workbench. An example would be ***sandpaper::create_lesson("/filepath/Carpentries Guide")***. This command
would create a new workbench with the name **Carpentries Guide** in the path you specified.



### sandpaper::draft_episode_md() & sandpaper::draft_episode_rmd()

This command takes in 1 input, that being the title of the episode you want to create. You would use this command when you have a
draft for an episode but don't yet want to publish it. It will create a template for the episode under the episodes/ folder and you can
edit it from there like a normal lesson. To do so, you will run the following command in the RStudio console, ***sandpaper::draft_episode_md("Episode Title")***. After you are completed and want to move the episode into the lesson, you will have to use the ***sandpaper::move_episode("Episode Name")*** 
command. This command will help you move the episode into the config file without you having to manually do it.
Of course, if you want to create an R Markdown episode use the ***rmd()*** otherwise use the ***md()***.

#### Before Episode Creation
![Episode Folder Before]({{ site.baseurl }}/assets/img/workbench/draft_before.png)

#### Episode Creation Command
![Episode Folder]({{ site.baseurl }}/assets/img/workbench/draft_command.png)

#### After Episode Creation
![Episode Folder After]({{ site.baseurl }}/assets/img/workbench/draft_after.png)

### sandpaper::create_episode_md() & sandpaper::create_episode_rmd()

These set of commands have the same functionality as the commands above except for the fact that you don't need to use the ***move_episode()*** function.
These commands will automatically create a new episode and input it into the config file so that you will be able to directly see any changes made
to it.

### sandpaper::serve()

Sandpaper::serve() is a command that will build and display your site in the bottom-right viewer of R Studio. (Tip: You can pop this view out
into it's own window) This command will incrementally update your Lesson as you make any changes. It is great for viewing changes in a quick manner
without having to constantly running ***sandpaper::build_lesson()*** or other build commands.

![Sandpaper::serve() and its Output]({{ site.baseurl }}/assets/img/workbench/sandpaper_serve.png)

If you look closely you a small icon to the right of the broom in the viewer window. If you click on that you will be able to pop-out the 
episode into a browser window.

![Pop-out Icon]({{ site.baseurl }}/assets/img/workbench/pop_out.png)

There are more ***sandpaper::*** commands if you browse around in the R Studio console but these are the most important ones that will be used.