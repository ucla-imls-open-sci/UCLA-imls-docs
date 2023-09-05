---
title: Add Button with Link
layout: default
parent: DataSquad Website Guide
nav_order: 2

---

# Adding Button with Link
1. **In the [Datasquad repository](https://github.com/UCLA-DataSquad/ucla-datasquad.github.io) (or it can be your local repository), navigate to `_data/sitetext.yml` file.**\
<img src="{{ site.baseurl }}/assets/img/datasquad-website-guide/add-link-btn/step1.jpg" alt="step1" width="400"/>

2. **In the section where you want to add the button, add the following lines:**
    - I will be referring to your desired section as `[your-desired-section]`. In my case, it will be the `about` section.
    ```
    button: [your-button-title]
    buttonlink: [your-desired-link]
    ```
    - Note that I will be adding the button in the `About` section, so I go to the `about` section in `sitetext.yml`, and add the follwing lines:
    ```
    button: Here's a button with a link
    buttonlink: https://github.com/UCLA-DataSquad/ucla-datasquad.github.io
    ```
    - what it should look like in the file: \
     <img src="{{ site.baseurl }}/assets/img/datasquad-website-guide/add-link-btn/step2.jpg" alt="step2" width="600"/>

3. **Navigate to `_includes/[your-desired-section].html`.**
<img src="{{ site.baseurl }}/assets/img/datasquad-website-guide/add-link-btn/step3.png" alt="step3" width="400"/>

4. **Paste the following lines:**

    ```
    {% raw %}
    {%- if site.data.sitetext[site.locale].[your-desired-section].button -%}
    <a class="btn btn-primary btn-xl text-uppercase js-scroll-trigger" href="{{ site.data.sitetext[site.locale].[your-desired-section].buttonlink }}">{{ site.data.sitetext[site.locale].[your-desired-section].button }}</a>
    {%- endif -%}
    {% endraw %}
    ```
    - Note that in the actual file, you need to change all `[your-desired-section]` to the actual section name where you want the button to be.
    - The file should look something like this. Notice that all `[your-desired-section]` has been changed to `about`:
    <img src="{{ site.baseurl }}/assets/img/datasquad-website-guide/add-link-btn/step4.png" alt="step4" width="600"/>

5. **Once you push your changes to the main branch, you should see the button in your desired section:**\
    - Make sure to click it and check that it links to a correct website!
    <img src="{{ site.baseurl }}/assets/img/datasquad-website-guide/add-link-btn/step5.png" alt="step5" width="800"/>

6. **Congrats! You added a button to the website! 🎉👏👏👏**