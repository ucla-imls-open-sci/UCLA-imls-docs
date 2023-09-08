---
title: Content Check Python
layout: default
parent: IMLS Tools
nav_order: 2
---

This tool is built ontop of the [content_check.sh]({{ site.baseurl }}/docs/imls-tools/content_shell). It has in interactive UI
and more options available.

You can find the python script at this [link](https://github.com/ucla-imls-open-sci/imls-tools/blob/main/content_check.py).

# Setting up the environment for the script

1. **Download the script or clone the repository**

2. **Check your python version to make sure its python 3.11**

    Run this command to check your python3 version `python3 --version`

    If it is not **Python 3.11** and you have a **Mac** run the following commands:
    ```
    # INSTALL HOMEBREW IF YOU DON'T HAVE IT
    $   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

    # INSTALL PYTHON 3
    $   brew install python3
    ```

3. **Download package dependencies**

    You need to download PySimpleGUI. Run the following commands:

    ```
    brew install python-tk
    pip3 install pysimplegui
    ```

# Running the script

Go to the following section depending on your needs:
1. [Lesson Downloaded]()
2. [No Lessons Downloaded]()
3. [Multiple Lessons Downloaded]()
4. [Check Episodes Folder]()
5. [Check config.yaml]()
6. [Check a single episode]()


1. **Run the Python Script**

    Run the script with the command `python3 content_check.py`.\
    It should display the following:

    ![Home]({{ site.baseurl }}/assets/img/imls-tools/python-1.png)

    

## **If you have a LESSON downloaded**
    
1. **Click on the browse button**

    It should display a file system for you to navigate.

    ![Browse]({{ site.baseurl }}/assets/img/imls-tools/python-2.png)

2. **Navigate to your LESSON folder**

    Navigate to the folder that you have your lesson in and click choose.
        
    ![Choose]({{ site.baseurl }}/assets/img/imls-tools/python-3.png)

3. **Click Run and read the output**

    ![Run]({{ site.baseurl }}/assets/img/imls-tools/python-4.png)
    
4. **Clear output and pick another folder and repeat**

    Pressing clear will clear the Results Window

    ![Clear]({{ site.baseurl }}/assets/img/imls-tools/python-5.png)



## **If you don't have a LESSON downloaded**

1. **Click the Remote Repo Button**

    It will open a pop-up where you can put the link to the remote repository.

    ![Remote Repo]({{ site.baseurl }}/assets/img/imls-tools/remote-1.png)

2. **Enter the URL to the remote Repository**

    Find the url to the remote repository on github. Then enter it into the text field and
    click search.

    ![Search]({{ site.baseurl }}/assets/img/imls-tools/remote-2.png)

3. **Click Run and read the output**

    ![Run Remote]({{ site.baseurl }}/assets/img/imls-tools/remote-3.png)



### *VERY IMPORTANT YOU HAVE TO CLOSE THE APPLICATION USING THE CLOSE BUTTON OTHERWISE THE TEMPORARY DIRECTORY IS NO LONGER TEMPORARY*


## **If you have multiple LESSON's downloaded**

1. **Open the directory that has the multiple lessons.**
    
    Click browse and find the directory that has all of the lessons.

    ![Directory]({{ site.baseurl }}/assets/img/imls-tools/mult-1.png)

2. **Click on the Lesson you want to run**

    Click on the lesson you want to run

    ![Click on Lesson]({{ site.baseurl }}/assets/img/imls-tools/mult-2.png)

3. **Click run**
    
    Click run

    ![Click run]({{ site.baseurl }}/assets/img/imls-tools/mult-3.png)


## **If you only want to check over the Episodes Folder**

1. **Click on the episodes folder**

    ![Click on Episodes]({{ site.baseurl }}/assets/img/imls-tools/python-6.png)

2. **Click Run**

    ![Episodes Only Run]({{ site.baseurl }}/assets/img/imls-tools/python-7.png)

## **If you only want to check over config.yaml**

1. **Click on the config.yaml file**

    ![config]({{ site.baseurl }}/assets/img/imls-tools/config-1.png)

2. **Click Run**

    ![config run]({{ site.baseurl }}/assets/img/imls-tools/config-2.png)


## **If you only want to check over a single episode**

1. **Click on the episode you want to run**

    ![episode]({{ site.baseurl }}/assets/img/imls-tools/ep-1.png)

2. **Click Run**

    ![episode run]({{ site.baseurl }}/assets/img/imls-tools/ep-2.png)