---
title: Add Lesson
layout: default
parent: IMLS Website Guide
nav_order: 4
---

# Adding a Lesson Entry
1. **In the [IMLS Repository](https://github.com/ucla-imls-open-sci/ucla-imls-open-sci.github.io) (or it can be a local repository) navigate to `_data/sitetext.yml`**\
<img src="{{ site.baseurl }}/assets/img/website-guide/add-lesson/step1.png" alt="step1" width="400"/>

2. **Under the `lessontab` section, add the following lines:**
```
  - lesson-title: 
    site: 
    repo:
    notes: 
    status:  
    author: 
```
- Make sure the indentation is correct!
- It should look like this:\
<img src="{{ site.baseurl }}/assets/img/website-guide/add-lesson/step2.png" alt="step2" width="600"/>

3. **Add content to your lesson**
    - `lesson-title`: Title of the lesson
    - `site`: Link to the lesson site
    - `repo`: Link to the repository of the lesson site
    - `notes`: Link to the notes page of the lesson site
    - `status`: Status of the lesson (pre-alpha, alpha, beta, or stable)
    - `author`: author(s) of the lesson\
    <img src="{{ site.baseurl }}/assets/img/website-guide/add-lesson/step3.png" alt="step3" width="600"/>

4. **After you push the changes to the main branch, you should see the new lesson entry in the table.**\
    - Make sure to click on each of the links to check that it's linked to a correct website!
    <img src="{{ site.baseurl }}/assets/img/website-guide/add-lesson/step4.png" alt="step3" width="800"/>

5. **Congrats! You just added a new lesson to the table. 🎉👏👏👏**
