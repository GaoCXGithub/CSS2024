# [Computational Social Science] 
## 1-2 Command Line Intro


# Working With The Command Line

You are probably used to interacting with your computer with **Graphical User Interfaces (GUIs)**. GUIs can make understanding and using software easy and intuitive, but come with some limitations too. Another way to interact with your computer is through the **Command Line Interface (CLI)**. CLIs allow you to interact with your computer directly through code. This feature has important implications for reproducibility and scientific research. Working with CLIs will enable you to work with big data, replicate code pipelines easily, and collaborate with other researchers efficiently.

## Instructions for Windows

Before we start with using the command line, Windows users will need to go through a couple of extra installation steps. macOS and Linux users can skip this section. Windows native command line, [Command Prompt](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands) has some unique syntax and may not work with everything we'll do in this course. Instead, we recommend installing [Git Bash](https://gitforwindows.org/). There are other options for Windows command line as well, but we recommend starting with Git Bash to make sure you have all of the git tools we'll need when we introduce GitHub. The steps for installation are:

1. Navigate to the [git for windows webpage](https://gitforwindows.org/), and click the "Download" buttom.

![Download Git for Windows](../images/Install_Git_for_Windows.png)

2. Run the Git installer. For the most part, keep the defaults that the installer recommends. Importantly, you should make sure to keep the recommended settings for adding git to your PATH,  and keeping the default behavior of git pull. The installer may ask if you want to install some beta features as well, we recommend not doing so as this could introduce some bugs.

![Click Next Through the Installer Options](../images/Git_Installer.png)


![Make sure Git is in your PATH](../images/Git_in_PATH.png)


![Keep the default "git pull" option](../images/Default_git_pull.png)


![Uncheck the Experimental Features](../images/Beta_features.png)

## Accessing the Command Line

For **Mac** users, you can access the command line by holding `Command + Space` and typing "terminal" into the spotlight. This is a keyboard shortcut that allows you to search any file on the computer very quickly. **Windows** users can either locate the Gitbash Icon on the desktop or click on the Windowns Icon navigate to the search bar in the lower left-hand corner of their screen and open Gitbash.

## Basic Command Line Prompts

Now we're ready to start working with the command line! See the table below for some common commands that we'll be using the course. We won't use too much advanced command line, but if you're intereested, this is a great [Software Carpentry tutorial](https://swcarpentry.github.io/shell-novice/index.html) that will provide you a great foundational grasp of the commmand line interface. I've found it very helpful in the past, and it's free. 

| Command | Description        | Example |
|---------|--------------------|---------|
| exit    | close the terminal | exit    | 
| cd      | change directory   | cd data | 
| cd -    | return to last directory   | cd - | 
| cd ..   | move up one folder | cd .. | 
| pwd     | print working directory | pwd |
| ls      | list files in directory | ls |
| cp      | copy file          | cp ../data/test.txt ../images/test.txt|
| mv      | move file          | mv ../data/test.txt ../images/test.txt|
| touch   | create a new file  | touch newfile.txt |
| mkdir   | make a new directory | mkdir newdir |
| rm      | delete a file      | rm test.txt |
| rm -r   | delete a directory | rm -r newdir |

Let's do the following together as a class:

1. Open a terminal and type "pwd" to see where you are. This will likely be the "home" directory, which is the default directory where you'll start when opening the terminal or Gitbash. 

2. Change your working directory to the "1 Installation and Reproducible Data Science" folder of this repository. If there are spaces in the folder name, it's easiest if you wrap the folder or filepath name in quotes.

2. Make a new directory called "newdir" using one of the commands from the table above and check to ensure it was created.

3. Copy "test.txt" from "1 Installation and Reproducible Data Science" to newdir and check to ensure it was copied. 

4. While in newdir, create a new file called "touch-testing.txt" using the "touch" method. Verify it was created. 

5. Delete the "touch-testing.txt" file, ensure it was deleted (make sure not to delete test.txt because we will need that soon), and then navigate back to the "1 Installation and Reproducible Data Science" directory.

## Using a text editor inside the command line

Navigate to newdir and find test.txt. Let's try to edit the "test.txt" file directly in the command line using a text editor. There are several different text editors. 
One good option is Vim. Vim is a lightweight text editor that will allow you to create and edit basic text files. Nano is another text editor that is common to use inside the command line. While you might mostly use text editors like Notepad, [Sublime](https://www.sublimetext.com/), or [Visual Studio](https://visualstudio.microsoft.com/) to edit large amounts of text, Vim or Nano can still be useful for making small edits and working with files on a server. 

First, type the following command:

	vim test.txt

Try following the instructions in the text file to add your name to the beginning of the file. You'll need to use the arrow keys to move the cursor. If you find that a little complicated, try it again using nano instead, which I find a bit easier to use. To activate nano, type:

	nano test.txt

## Running a Python Script

The last thing we will cover is using the command line to run Python code. We won't have you regularly do this for this course, but it is useful to know this is an option if you ever are working with a remote server. This is a fairly common situation when you are working with sensitive or restricted-access data (i.e. medical records) or big data.

First, use `touch` to create a file called "hello.py".


	touch hello.py

Now check the files in your current working directory to see if it's there. If so, use vim to add the following text:

	#!/usr/bin/env python3
	print('Hello World!')

Exit the vim editor, and then in the command line, run the following:

	python3 hello.py

or if that doesn't work, try:

	python hello.py

What happens when you run this? Ideally, it should have printed "Hello World!" to the console! As you progress with your coding skills, your projects may require you to run complicated Python scripts for long periods of time. Being able to run them on remote servers, or chain together many different scripts together will be a key skill in helping you manage that workflow.

## Challenge Question

Accomplish the following tasks using only the command line interface:

1. Create a folder named "challenge" inside of your "newdir" directory.

2. cd into this directory

3. Inside of the challenge directory, create a file named movies.txt

4. Add the name of your favorite movie to this file

5. Copy this file to your Desktop

6. Delete the file from your challenge folder

7. Show the contents of movies.txt on your screen

8. Open movies.txt

BONUS: What happens if you try to delete the challenge folder while there is still a file inside of it?
