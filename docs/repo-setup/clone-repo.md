---
title: Clone a Repository to your Local Device
layout: home
parent: Lesson Repository Setup
nav_order: 2
---

# Clone a Repository to your Local Device
1. Fork the [Workbench Markdown template](https://github.com/new?template_name=workbench-template-md&template_owner=carpentries) into your desired organization. You can select an organization from the drop down arrow in Owner. Please name the repository to reflect your lesson proposals.\
![Create a new Repository]({{ site.baseurl }}/assets/img/repo-setup/clone-repo1.png)
2. Clone the repository to your local device. Open R studio, and go to `File -> New Project -> Version Control -> Git`.
![file -> new project]({{ site.baseurl }}/assets/img/repo-setup/clone-repo2a.png)\
![go to Version Control]({{ site.baseurl }}/assets/img/repo-setup/clone-repo2b.png)\
![choose Git]({{ site.baseurl }}/assets/img/repo-setup/clone-repo2c.png)
3. The repository URL is the GitHub website link to your repository.
    - paste the URL, and name the folder. This should clone the repository onto your local device successfully.\
    ![Your GitHub repo link]({{ site.baseurl }}/assets/img/repo-setup/clone-repo3a.png)\
    ![Paste the URL here.]({{ site.baseurl }}/assets/img/repo-setup/clone-repo3b.png)
4. Connect your local device to your Online Repository
    - Run `git config remote.origin.url git@github.com:[your-github-username]/[your-online-repo-name].git` in the R Studio Terminal. You can find the link from the online repository.\
    ![Paste the URL here.]({{ site.baseurl }}/assets/img/repo-setup/clone-repo4.png)
    - NOTE: If it is your first time adding a SSH key, it will ask you if you want to build a connection. You should answer yes. 
5. You have successfully connected your local device to the online repository. Congratulations!




