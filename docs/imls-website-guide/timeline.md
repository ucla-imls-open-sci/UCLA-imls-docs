---
title: Timeline
layout: default
parent: IMLS Website Guide
nav_order: 5
---

# Changing the Timeline

1. **In the [IMLS Repository](https://github.com/ucla-imls-open-sci/ucla-imls-open-sci.github.io) navigate to `_data/sitetext.yml`**

    ![_data/sitetext.yml]({{ site.baseurl }}/assets/img/website-guide/timeline-1.png)

2. **Find the "timeline" section**

    You can do this with `ctrl/cmd + f timeline`
    ![timeline section]({{ site.baseurl }}/assets/img/website-guide/timeline-2.png)

3. **Add or Remove a Timeline**
    You can do so by copying a timeline object and altering the fields
    1. `title:` Title of the new event/object
    2. `year:` The time-dates of the event/object
    3. `desc:` A description of the event/object
    4. `image:` A reference to the image you want to display
    5. `alt:` An alternative for the image in case it doesn't load

    ![Add Timeline]({{ site.baseurl }}/assets/img/website-guide/timeline-3.png)

4. **After you push the changes to the main branch, you should see the new timeline entry in the list.**
    ![Timeline Webpage]({{ site.baseurl }}/assets/img/website-guide/timeline-4.png)