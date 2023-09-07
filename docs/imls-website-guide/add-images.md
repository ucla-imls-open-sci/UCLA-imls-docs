---
title: Add image
layout: default
parent: IMLS Website Guide
nav_order: 3
---



# Adding images 
1. Navigate to `assets/img`, where the images of the website is stored. The folder is further organized into authors, clients, committees, portfolio, and staff. 
![asset/image folder]({{ site.baseurl }}/assets/img/website-guide/add-image-1.png)

2. Upload the image (preferably as png or jpeg) to the appropriate folder. 

![appropriate image folder]({{ site.baseurl }}/assets/img/website-guide/add-image-2.png)

3. To disply the image: 
    - in `.md` files:  ``` ![Alt text]({{site.baseurl}}/assets/img//image-name.png)" ```
    - in `.html` files: ``` img src="{{site.baseurl}}/assets/img//image-name.png" ```
    - in `.yml` files: type in the file path 

    For example: this line in `sitetext.yml`: 

    ![sitetext image code]({{ site.baseurl }}/assets/img/website-guide/add-image-3.png)

    results in the following display on the website: 

    ![image display]({{ site.baseurl }}/assets/img/website-guide/add-image-4.png)






