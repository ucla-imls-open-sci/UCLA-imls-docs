---
title: Callout Blocks
layout: default
parent: Carpentries Workbench
nav_order: 2
---

The Carpentries Workbench comes with a customized version of Pandoc. What is pandoc? Pandoc is a tool that allows for custom callout blocks.
These blocks can be used in a variety of ways from challenge questions to discussion points. A formative list of all the [Callout Blocks](https://carpentries.github.io/sandpaper-docs/component-guide.html) supported by the Carpentries are found in that link.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Callout Blocks

Callout blocks are created through ***fenced divs***. These are a pair of 3 or more ***:::*** at the beginning and end of what you are 
trying to callout.

![Default Callout Block]({{ site.baseurl }}/assets/img/workbench/default_callout.png)

The code for this callout block goes as follows:

```
::: callout 
## Callout Block
This is what a default Callout block looks like
:::
```

The structure of the callout block starts with at least 3 colons (:::) followed by the type of callout that you want to use. You can find a list of
supported callout blocks [here](https://carpentries.github.io/sandpaper-docs/component-guide.html). After that comes the content followed by an ending set of colons. 

<i> Note that you don't need to have exactly 3 colons, you need ***AT LEAST*** 3 colons in order to create a callout block. </i>

```
::: Name of the callout block you want to use
## Heading
Content
::: <- ending set of colons
```

## Special Callout Blocks

### Questions and Objectives
Every episode should contain a ***questions*** and ***objectives*** callout block at the start. This outlines an overview for the episode that is
being taught. They are displayed side by side in the browser and will look like this.

![Questions and Objective Callout Block]({{ site.baseurl }}/assets/img/workbench/Q_O.png)

The code for this looks like this:

```
::: questions
- How do you write a lesson using Markdown and `{sandpaper}`?
:::
::: objectives
- Explain how to use markdown with The Carpentries Workbench
- Demonstrate how to include pieces of code, figures, and nested challenge blocks
:::
```

*Note that these two callout blocks are special and have to follow each other in order to be displayed properly. Another thing
to note is that they are using markdown's bullet point format putting '-' in the beginning of each statement.*

### Challenges
Challenges should be frequently utilized throughout a lesson. The Carpentries has a special Challenge block that looks like this.

![Challenge Block]({{ site.baseurl }}/assets/img/workbench/challenge.png)

The ***Challenge*** block is accompanied by a ***solution*** block with the ability to add a ***hint*** block as well. the code for that
looks something like this.

```
:::::::::::::::::::::::::::::::::: challenge
## Challenge title (optional)
Challenge
::::::::::::::::::: hint
your hint
:::::::::::::::::::
::::::::::::::::::: solution
### Title (optional)
Solution
:::::::::::::::::::
::::::::::::::::::::::::::::::::::
```

In this callout block, we nest the ***solution*** and ***hint*** blocks within the ***challenge*** block. This is so the heirarchy is
preserved. Another thing to note is the Title in ***solution*** block. If you choose to include a title then the title would replace the
***SOLUTION*** tab with the title that you give it. Another thing is that a ***challenge*** block should be accompanied by a ***solution*** block but that is optional. The ***hint*** block is completely optional and up to user descretion.

<i>Note that the solution and hint tabs will be closed at first. </i>

There are several other callout blocks that are supported and you can find more information about them [here](https://carpentries.github.io/sandpaper-docs/component-guide.html)