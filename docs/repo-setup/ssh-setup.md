---
title: Set up your SSH key
layout: home
parent: Lesson Repository Setup
nav_order: 1
---

# Create SSH Key and Connect Your Local Device to an Online Repository
1. **Install [git(Mac)](https://carpentries.github.io/workshop-template/#shell-windows) / [git(Windows)](https://carpentries.github.io/workshop-template/#shell-windows), [R](https://carpentries.github.io/workshop-template/#shell-windows), and [R Studio](https://posit.co/download/rstudio-desktop/#download).**
    - If you have git installed, use `git –-version` to check the version of git. 
    - Git Version 2.41.0 is recommended, but not required.
        - Mac: Use `brew upgrade git` to update to the latest version.
        - Windows: Use `git update-git-for-windows` to update git to the latest version.
1. **Install Required Packages in R Studio Console**\
    ![img]({{ site.baseurl }}/assets/img/repo-setup/1.jpg)\
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
1. **Link to Git in R Studio**
    - Tools -> Global Options\
    ![img]({{ site.baseurl }}/assets/img/repo-setup/2a.png)
    - Link the git.exe to Git executable\
    ![img]({{ site.baseurl }}/assets/img/repo-setup/2b.png)
1. **Generate SSH key in R Studio**
    - Tools -> Global Options\
    ![img]({{ site.baseurl }}/assets/img/repo-setup/3a.png)
    - When you create an SSH key, it generates two files. One is a private file that can only be used on your local machine, and another one is the public key that needs to be added to your github account. 
1. **Copy Public Key**
    - Click on "View public key" to copy your public key\
    ![img]({{ site.baseurl }}/assets/img/repo-setup/4.png)

1. **Add Public Key to your GitHub Account**
    - Settings -> SSH and GPG keys\
    ![img]({{ site.baseurl }}/assets/img/repo-setup/5a1.png)\
    ![img]({{ site.baseurl }}/assets/img/repo-setup/5a2.png)
    - Click on New SSH Key. Name it, and paste the public SSH key that was copied earlier.
1. **Add SSH key to SSH agent.**
    - Open Terminal in R Studio, and run these commands:
    ```
    eval $(ssh-agent -s)
    ssh-add ~/.ssh/id_ed25519
    ssh -T git@github.com
    ```
    - If you’re on macOS Sierra 10.12.2 and higher, you need to do one more thing. Create a file `~/.ssh/config` with these contents:\
    ```
    Host *
        AddKeysToAgent yes
        UseKeychain yes
        IdentityFile ~/.ssh/id_ed25519
    ```
1. **Test if you added SSH key successfully**
    - Run `ssh -T git@github.com`


