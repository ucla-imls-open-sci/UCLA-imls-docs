---
title: IMLS Website Guide
layout: default
permalink: /docs/website-guide
has_children: true
nav_order: 5
---

# Website Guide



This guide should cover managing the website, executing on the grant (administrative and logistical), repo setup, anything about lesson support.

Here is an annotated screenshot overview of the IMLS website gituhb repository.
![Overview of IMLS doc structure]({{ site.baseurl }}/assets/img/website-guide/UCLA IMLS Website Repo Overview.png)


Before learning to edit and update the website, it's better to have a basic understanding of the folder structure so you know where to go. Here is a list of the most relevant folders and files of the jekyll directory structure, and a brief explanation of what each does. 

- `_config.yml`
is a YAML file that stores configuration data, which include site settings and rarely changed variables (name, description, etc.)
> note: folders that starts with a "_" are special folders associatedwith the jekyll template. Every other directory/file such as `css` files and `images` folder are generate verbatim to site. 

- **`_data`**: 
contains well-formatted site data. Jekyll automatically loads its children files (in `.yml`, `.yaml`, `.json`, `.csv` or `.tsv`) to be accessible via `site.data`. (To access contents of a file: for a file named `members.yml`, use code `site.data.members`)
    - `navigation.yml` navigation for the pages
    - `sitetext.yml` edit text for the website here 
    - `style.yml`

- `_includes`:
partial html pages mixed and matched by layouts and posts to facilitate reuse. 
    
- `_layouts`:
html templates that wrap posts, chosen on a post-by-post basis in the front matter. 

- `_posts`: 
contain blog posts for the website.

## Making Changes Locally

If you plan to making and previewing changes locally rather than working directly on github.com, go through the 
[*Local Environment guide*]({{ site.baseurl }}/docs/imls-website-guide/local-env/local-env.html) first.
