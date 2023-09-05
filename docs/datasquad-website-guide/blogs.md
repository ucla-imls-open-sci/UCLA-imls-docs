---
title: Add/Manage Blogs
layout: default
parent: DataSquad Website Guide
---

# Adding Blogs

1. Navigate to the `_posts` directory

2. On the top right corner: Add file -> create new file 

    ![create new blog]({{ site.baseurl }}/assets/img/datasquad-website-guide/add-blogs/add-blog-2.png)
    
    **Note** The naming convention of these .md files is important, and must follow the format: '`YEAR-MONTH-DAY-title.MARKUP`'. The permalinks can be customized for each post, but the date and markup language are determined solely by the file name.

3. Update the title, layout and author of the file

    ![update blog information]({{ site.baseurl }}/assets/img/datasquad-website-guide/add-blogs/add-blog-3.png)

4. Your new blog should now show up on the website after you push and deploy your changes! 

    ![blog post displayed on site]({{ site.baseurl }}/assets/img/datasquad-website-guide/add-blogs/add-blog-4.png)

# Highlighting Blogs

To highlight a blog, add this section to the top of the post.

![Blog Highlight Front-matter]({{ site.baseurl }}/assets/img/datasquad-website-guide/add-blogs/highlight-1.png)

1. You need to have ``` showcase: 1 ```, this will signifiy that you wan the blog highlighted.

2. You need to add the ``` card ``` section. This section is exactly like a project card except for the last two variables. Refer to [Add Projects]({{ site.baseurl }}/docs/datasquad-website-guide/add-blogs/add-projects)

3. ``` intro: ``` This is what is going to be displayed on the blog card. Write a short introduction to the blog here.

4. ``` url: ``` The url should be the date followed by the file name in the following format: ```YYYY/MM/DD/File_name```

After adding this to a blog post, it should appear like the following on the webpage:

![Blog Card]({{ site.baseurl }}/assets/img/datasquad-website-guide/add-blogs/highlight-2.png)

![Blog Card]({{ site.baseurl }}/assets/img/datasquad-website-guide/add-blogs/highlight-3.png)