---
title: Content Check Shell
layout: default
parent: IMLS Tools
nav_order: 1
---

This is a shell script that was developed to check and validate Lesson contents. There is a python script that is more intuitive but
if you are on a virtual environment you can run this script easier.

You can find the shell script at this [link](https://github.com/ucla-imls-open-sci/imls-tools/blob/main/content_check.sh)

*NOTE this script may also be incomplete*

*NOTE if you don't want to go through this documentation, you can run `./content_check.sh --help` it will print out a manual for you*

1. **Download the script or clone the repository**

2. **If you haven't already, give the script execute access**

    You can do so by running the code: `chmod +x content_check.sh` in the directory that
    has the script.

3. **Run the script**

    1. **Base Script**
        The script has many options that help it run. To run the base script you will need to use the option `-P`.
        Run the following code in order to get its base functionality to work.

        ```
        ./content_check.sh -P <path_to_lesson_directory>

        # Example
        $   ./content_check.sh -P ./c-_guide
            Lesson Title: Programming in C++

            Config.yaml Validation:
                Title: Programming in C++
                Contact: Invalid
                Created: 2023-07-19
                Source: https://github.com/lawtlee/c-_guide

            Episode Validation:
                Episode: hello-world.Rmd
                    Questions: Valid
                    Objectives: Valid
                    Keypoints: Valid
                Episode: introduction.Rmd
                    Questions: Valid
                    Objectives: Valid
                    Keypoints: Valid
                Episode: test.md
                    Questions: Valid
                    Objectives: Valid
                    Keypoints: Valid
                Episode: variables.Rmd
                    Questions: Valid
                    Objectives: Valid
                    Keypoints: Invalid
        ```
        *NOTE be aware of spaces in your file paths, it may lead to problems*

        The script will run a check over the **config.yaml** file and the **episodes** folder and check if they have the required points.
    
    2. **Aditional Options**
        1. **-C, --challenges**

            This flag will display the number of **Challenges** in each episode.
            ```
            $   ./content_check.sh -P ./c-_guide -C
                Lesson Title: Programming in C++

                Config.yaml Validation:
                    Title: Programming in C++
                    Contact: Invalid
                    Created: 2023-07-19
                    Source: https://github.com/lawtlee/c-_guide

                Episode Validation:
                    Episode: hello-world.Rmd
                        Questions: Valid
                        Objectives: Valid
                        Keypoints: Valid
                        Number of Challenges:  2
                    Episode: introduction.Rmd
                        Questions: Valid
                        Objectives: Valid
                        Keypoints: Valid
                        Number of Challenges:  0
                    Episode: test.md
                        Questions: Valid
                        Objectives: Valid
                        Keypoints: Valid
                        Number of Challenges:  1
                    Episode: variables.Rmd
                        Questions: Valid
                        Objectives: Valid
                        Keypoints: Invalid
                        Number of Challenges:  0
            ```

        2. **-S, --solutions**

            This flag will display the number of **Solutions** in each episode.
            ```
            $   ./content_check.sh -P ./c-_guide -C
                Lesson Title: Programming in C++

                Config.yaml Validation:
                    Title: Programming in C++
                    Contact: Invalid
                    Created: 2023-07-19
                    Source: https://github.com/lawtlee/c-_guide

                Episode Validation:
                    Episode: hello-world.Rmd
                        Questions: Valid
                        Objectives: Valid
                        Keypoints: Valid
                        Number of Discussions:  2
                    Episode: introduction.Rmd
                        Questions: Valid
                        Objectives: Valid
                        Keypoints: Valid
                        Number of Discussions:  0
                    Episode: test.md
                        Questions: Valid
                        Objectives: Valid
                        Keypoints: Valid
                        Number of Discussions:  2
                    Episode: variables.Rmd
                        Questions: Valid
                        Objectives: Valid
                        Keypoints: Invalid
                        Number of Discussions:  0
            ```
        3. **-D, --discussions**

            This flag will display the number of **Discussions** in each episode.
            ```
            $   ./content_check.sh -P ./c-_guide -C
                Lesson Title: Programming in C++

                Config.yaml Validation:
                    Title: Programming in C++
                    Contact: Invalid
                    Created: 2023-07-19
                    Source: https://github.com/lawtlee/c-_guide

                Episode Validation:
                    Episode: hello-world.Rmd
                        Questions: Valid
                        Objectives: Valid
                        Keypoints: Valid
                        Number of Solutions:  0
                    Episode: introduction.Rmd
                        Questions: Valid
                        Objectives: Valid
                        Keypoints: Valid
                        Number of Solutions:  0
                    Episode: test.md
                        Questions: Valid
                        Objectives: Valid
                        Keypoints: Valid
                        Number of Solutions:  0
                    Episode: variables.Rmd
                        Questions: Valid
                        Objectives: Valid
                        Keypoints: Invalid
                        Number of Solutions:  0
            ```

        4. **-o \<file\>**

            This flag specifies an output file. it will ouput into a file instead of the terminal

            ```
            # Terminal
            $   ./content_check.sh -P ./c-_guide -o test.txt

            # test.txt
                Lesson Title: Programming in C++

                Config.yaml Validation:
                    Title: Programming in C++
                    Contact: Invalid
                    Created: 2023-07-19
                    Source: https://github.com/lawtlee/c-_guide

                Episode Validation:
                    Episode: hello-world.Rmd
                        Questions: Valid
                        Objectives: Valid
                        Keypoints: Valid
                    Episode: introduction.Rmd
                        Questions: Valid
                        Objectives: Valid
                        Keypoints: Valid
                    Episode: test.md
                        Questions: Valid
                        Objectives: Valid
                        Keypoints: Valid
                    Episode: variables.Rmd
                        Questions: Valid
                        Objectives: Valid
                        Keypoints: Invalid
            ```

        *NOTE the -e flag has depreciated and is now moved into the python script*

4. **Debugging/problems**

    If you run into any issues create a new Issue in the repository and flag **@lawtlee**. 
    Provide a picture of what went wrong as well.