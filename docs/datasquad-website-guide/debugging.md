---
title: Debugging
layout: default
parent: DataSquad Website Guide
---

If you have any issues with either your blog highlight or project card showing up read this documentation.

## Check Github Actions
First, check for any **Github Action** errors. If there are any errors it may mean that the workflow designed to update
the site failed. To navigate to the potential source of error follow the steps below:

1. Navigate to **Github Actions** in the [DataSquad Site Repo](https://github.com/UCLA-DataSquad/ucla-datasquad.github.io)

    ![Github Actions]({{ site.baseurl }}/assets/img/datasquad-website-guide/debugging/actions-1.png)

2. Look at the most recent workflows, if there is no workflow with an X then that means everything completed perfectly and you can move on. 
If not it looks like:

    ![Workflow]({{ site.baseurl }}/assets/img/datasquad-website-guide/debugging/actions-2.png)

3. Click on the failed workflow and look through it and see what failed. If the workflow failed because of jekyll being unable to run
that means that there is code in your most recent commit that breaks jekyll. Look through the changes you've made and try to identifiy any code
that may have done so. If you click deeper into the workflow it may tell you what the error is.

    ![Workflow Error]({{ site.baseurl }}/assets/img/datasquad-website-guide/debugging/actions-3.png)
    ![Workflow Error Details]({{ site.baseurl }}/assets/img/datasquad-website-guide/debugging/actions-4.png)

## Check the Repository

Now if your workflow error has a specific about what went wrong with jekyll follow the error message and locate your bug. If your workflow error has
nothing to do with jekyll or it has no error at all follow the steps below. If you don't care how it works skip to **step 5**

1. **Count the number of files in the _posts folder.**

    The following example has 5 posts.
    
    ![Post Count]({{ site.baseurl }}/assets/img/datasquad-website-guide/debugging/repo-1.png)

2. **Check the _includes/modals.html file.**

    Look for the following line of code  \
    {% raw %} `{% assign modified_index = forloop.index | plus: %}`. {% endraw %} 
    You can `ctrl/cmd + f` the following to find it: `assign modified_index`
    
    ![modals.html]({{ site.baseurl }}/assets/img/datasquad-website-guide/debugging/repo-2.png)

    Notice how the number after `plus` doesn't align with the number of blog posts. The error exists here and you should change it to the appropriate
    number of blogs.

3. **Check the _includes/portfolio_grid.html file.**
    
    Look for the same line of code as _includes/modals.html If there are any discrepancies with the code make that fix.

4. Run Jekyll locally with the `bundle exec jekyll serve` command and see if your blog/project appears.

5. To avoid doing all of that work you can just run the *blog_script,sh* with the following command:
    `./blog_script.sh`

If this does not solve your issue, then you will have to debug for the issue on your own. A good start is to look at the files
you have added/modified and work backwards from there until you reach the source of error.