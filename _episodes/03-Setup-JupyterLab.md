---
title: "Setting up Python and Jupyter Lab"
teaching: 5
exercises: 0
questions:
- "How do I setup Python to be accessible on COLA computers?"
- "What is JupyterLab?"
- "How do I setup JupyterLab on COLA computers?"
objectives:
- "Explain why we need to setup and configure Python"
- "Explain what JupyterLab is and why we are using it"
- "Explain how to setup JupyterLab on COLA servers"
- "Explain what you can do with JupyterLab"
keypoints:
- "Python requires packages to be imported"
- "A Python environment sets up the packages that are available"
- "JupyterLab is an interactive Python interface that is ideal for scientific work"
---
### Why do I need to setup a Python environment?

### COLA Computers

The Center for Ocean-Land-Atmosphere Studies (COLA) in the Department of Atmospheric, Oceanic, and Earth Sciences (AOES) has Linux computers used to analysis of Climate Data.  They consist of cola1, cola2, cola3, ... , cola7.  These are the computers we will use in this class.  

### Setting up Software for your computer

To login to the COLA computers, you need secure shell (ssh) software. The software differs based on what type of computer you have. 

#### macOS
For a Mac computer, use software called [Xquartz](https://www.xquartz.org/)
#### Windows
For a Windows computer, use software called [MobusXterm](https://mobaxterm.mobatek.net/)

> ## Download and install the correct ssh software for your computer
>
> Download the correct software for your computer 
> Follow the instructions on your computer to install the software
>
{: .challenge}

> ## In this class, you can
>
> * Raise your hand when you need assistance or have a question
> * Indicate you are done with a Challenge in the colaborative document
>
.{callout}

### Logging in

You received a username and password from our system administrator.  You will need this to login to the COLA computers.

#### On _macOS_
Launch the XQuartz software you downloaded and select `Shell`-> `New Window` from the menu in the upper left.
A window will appear that looks something like (look may vary depending on version of macOS and/or some default settings in `Xquartz`):

![Xquartz window](https://github.com/kpegion/AOES-CLIM-intro-cola-computing/blob/gh-pages/assets/img/Xquartz-open.png)

To connect to the computer `cola1` , type the following and replace `username` with your username:

~~~
$ ssh -Y -l username@cola1.gmu.edu
~~~
{: .language-bash}

Enter your password when prompted.
You will now be required to change your password.  

#### On Windows
1. Launch the MobusXterm software you downloaded.  
2. Click `Session`->`SSH` 
3. In the `Remote host` box, enter `cola1.gmu.edu` 
4. Check the `Specify username` box and enter your `username`
5. Click OK
6. Enter your password when prompted
7. Select No when asked to save your password.  

You will now be required to change your password.  Follow the prompts change your password.

> ## Password Requirements
>
> * [Password Complexity] (https://its.gmu.edu/working-with-its/it-security-office/it-security-standards/password-complexity-standard/)
> * Keep your password secure and in a safe place
> * Do not share your password.
> * Do not store your password in plain text. 
> * Follow the Mason [Responsible Use of Technology Policies] (https://universitypolicy.gmu.edu/policies/responsible-use-of-computing/)
>
.{callout}

> ## Login to a different COLA computer
>
> COLA computers are cola1, cola2, cola3, ... , cola7
> Choose a computer other than cola1 and login to it.
>
{: .challenge}
