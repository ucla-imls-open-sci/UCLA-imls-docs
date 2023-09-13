---
title: Add Contact Form
layout: default
parent: IMLS Website Guide
nav_order: 7
---

# Adding a Contact Us form using Calendly
1. **Log-in to Calendly**
2. **Navigate to ["Routing" section of Calendly website](https://calendly.com/app/routing/forms/user/me)**
3. **Find the form you want to add to the website.**
    - This tutorial will use "IMLS Meeting" form in the red box.

    <img src="{{ site.baseurl }}/assets/img/website-guide/add-contact-form/step1.png" alt="step3" width="600"/>
4. **Click on the "Share" button of the form.**\
    <img src="{{ site.baseurl }}/assets/img/website-guide/add-contact-form/step2.png" alt="step4" width="600"/>
5. **In the pop-up, click on the "Add to website" tab and select "Inline Embed"**\
    <img src="{{ site.baseurl }}/assets/img/website-guide/add-contact-form/step3.jpg" alt="step5" width="600"/>
6. **Customize the colors as you desire, and copy the code provided using the "Copy Code" button at the bottom right**\
<img src="{{ site.baseurl }}/assets/img/website-guide/add-contact-form/step4.png" alt="step6" width="600"/>

7. **Navigate to the repository of your website.**
8. **In the `_includes` folder, create a new `html` file.**\
- I will refer to the file name as `[your-file-name]`.
<img src="{{ site.baseurl }}/assets/img/website-guide/add-contact-form/step5.png" alt="step8" width="600"/>

9. **Paste the code below into the `[your-file-name].html` file you created.**
    - Delete the line `<!-- PASTE YOUR CODE HERE -->` and paste the code that you copied from Calendly.

    ```
    {% raw %}
    <section class="bg-light page-section" id="{{ site.data.sitetext[site.locale].contact.section | default:"contact" }}">
        <div class="container">
            <div class="row">
                <div class="col-lg-12 text-center">
                    <h2 class="section-heading text-uppercase">{{ site.data.sitetext[site.locale].contact.title }}</h2>
                </div>
            </div>
        <!-- PASTE YOUR CODE HERE -->
        </div>
    </section>
    {% endraw %}
    ```
10. **In the `_data/navigation.yml` file, add a new title and section under the `nav` section.**
```
- title: "Contact Us"
  section: [your-file-name]
```
- **IMPORTANT**: Make sure that the `section:` name matches the name of the html file `[your-file-name]` that you created!!\
<img src="{{ site.baseurl }}/assets/img/website-guide/add-contact-form/step6.png" alt="step10" width="600"/>

11. **In the `_data/sitetext.yml` file, add the following text.**
- Make sure `title` and `section` is indented as shown in the image below.
```
[your-file-name]:
    title: "Contact Us"
    section: [your-file-name]
```
- **IMPORTANT AGAIN**: Make sure that the `section:` name matches the name of the html file `[your-file-name]` that you created!!\
<img src="{{ site.baseurl }}/assets/img/website-guide/add-contact-form/step7.png" alt="step11" width="600"/>

12. **In the `_layouts/home.html`, add `{% raw %}{% include [your-file-name].html %}{% endraw %}`.**\
<img src="{{ site.baseurl }}/assets/img/website-guide/add-contact-form/step8.png" alt="step12" width="600"/>

13. **You should be able to see your form on the website. [(example)](http://ucla-imls-open-sci.info/#contact)**\
<img src="{{ site.baseurl }}/assets/img/website-guide/add-contact-form/step9.png" alt="step13" width="600"/>

14. **Congrats! You just added a new Calendly Contact Us form to the website!! 🎉👏👏👏**
