---
title: Set up your SSH key
layout: home
parent: Lesson Repository Setup
---

# Create SSH Key and Connect Your Local Device to an Online Repository
1. **Install [git(Mac)](https://carpentries.github.io/workshop-template/#shell-windows) / [git(Windows)](https://carpentries.github.io/workshop-template/#shell-windows), [R](https://carpentries.github.io/workshop-template/#shell-windows), and [R Studio](https://posit.co/download/rstudio-desktop/#download).**
    - If you have git installed, use `git –-version` to check the version of git. 
    - Git Version 2.41.0 is recommended, but not required.
        - Mac: Use `brew upgrade git` to update to the latest version.
        - Windows: Use `git update-git-for-windows` to update git to the latest version.
1. **Install Required Packages in R Studio Console**
    - Navigate to R Studio, and then go to console, and run these commands:
        - `CRANoptions(repos = c(carpentries = "https://carpentries.r-universe.dev/", CRAN = "https://cran.rstudio.com/"))`
        - `install.packages(c("sandpaper", "varnish", "pegboard","tinkr"))`
1. **Test the installation in R Studio Console**
    ```
    rmarkdown::pandoc_version() 
    tmp <- tempfile() 
    sandpaper::no_package_cache()
    sandpaper::create_lesson(tmp, open = FALSE)
    sandpaper::build_lesson(tmp, preview = FALSE, quiet = TRUE)
    fs::dir_tree(tmp, recurse = 1)
    ```
1. Link to Git in R Studio
    - Tools -> Global Options
    
