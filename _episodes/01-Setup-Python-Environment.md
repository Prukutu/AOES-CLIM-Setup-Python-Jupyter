---
title: "Setting up a Python Environment"
teaching: 5
exercises: 0
questions:
- "How do I setup my own Python environment on COLA?"
objectives:
- "Explain why we need to setup and configure Python environments"
- "Explain how to setup a Python environment"
- "Setup the Python environment for this class"
keypoints:
- "Python requires packages to be imported"
- "A Python environment defines packages that are available for import"
- "A Python environment is invoked using the `conda activate` command"
- "Activate the Python environment for this class with `conda activate aoes` whenever you login to COLA computers"
---
### Why do I need to setup a Python environment?
Python requires users to `import` packages to be used and almost everything requires a package. Recall in the previous lesson, we used the `import numpy` command.  We were able to do this because `numpy` is setup on the COLA computers. That is not always the case. Here's an example:

There is a meteorological Python package called [`MetPy`](https://unidata.github.io/MetPy/latest/index.html). I found an example under `Getting Started with MetPy` that I want to use in my code. Let's try it out and see what happens:

~~~
import numpy as np
from metpy.units import units

distance = np.arange(1, 5) * units.meters

~~~
{: .language-python}

~~~
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ModuleNotFoundError: No module named 'metpy'
~~~
{: .error}
What happened?  `MetPy` is not installed on the COLA computers.  What can we do about it?  We can setup our own Python environment that allows use to control what packages and versions are available to import in our Python programs.

Some other reasons why we need our own Python environment rather than relying on the default installation on COLA computers:
* I found a nice example for plotting my data by searching the internet and I tried it, but the Python package in the example is not installed on COLA computers.  
* I found a function in a Python package that does exactly what I need.  It would save me so much time to use it rather than write my own, but the package version on the COLA computers is old and does not have this new function. 
* I want to preserve the exact packages and versions of packages I used in my data analysis so that others can use my codes or so I can reproduce all my analysis when my paper comes back from review.


## Install our own Python environment

1. Log into a COLA Server and execute the following from the Unix shell in your home directory

~~~
$ git clone https://github.com/kpegion/Pangeo-at-AOES.git
~~~
{: .language-bash}

This gets some files from a code repository I created on Github. Before we go further in setting up our environment, let's take a look and see what this repository is and what we downloaded.

> ## Be careful what you download
>
> Its a good idea to be careful about what we download.  Fortunately, I would not have you download anything
> dangerous.  To see for yourself where we downloaded from, 
> go to https://github.com/kpegion/Pangeo-at-AOES.git in your web browser and take a look.
>
{: .discussion}

2. Change directory to Pangeo-at-AOES
~~~
$ cd Pangeo-at-AOES 
~~~
{: .language-bash}

> ## Take a look at what you downloaded
>
> Use your knowledge of Unix commands to see what is in the Pangeo-at-AOES directory
>
> The file that we are going to use to set up our Python environment is called `environment.yml`
> What Unix commands could you use to see what is in this file?
>
{: .challenge}

3. Load the version of Python installed on the COLA Computers
~~~
$ cd module load anaconda/3
~~~
{: .language-bash}

4. Create your Python environment
~~~
$ conda env create -f environment.yml
~~~
{: .language-bash}

5. Execute the following command so that your new environment is not initialized by default on login
~~~
$ conda config --set auto_activate_base false
~~~
{: .language-bash}

6. Activate the environment so you can work in Python with the packages:
~~~
$ conda activate aoes
~~~
{: .language-bash}

## What to do now that my environment is setup

These were steps for setting up the Python environment. Now that you have done them, next time you login to COLA computers, all you need to do is the final step of activating the environment.  

> ## Login and activate your environment
>
> Logout of COLA computers and log back in.
> Activate your Python environment.
> Run the `metpy` example again.
>
{: .challenge}

