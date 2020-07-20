---
title: "Setting up Python and Jupyter Lab"
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
- "An environment is invoked using the `conda activate` command"
---
### Why do I need to setup a Python environment?
Python requires users to `import` packages to be used and almost everything requires a package. Recall in the previous lesson, we used the `import numpy` command.  We were able to do this because `numpy` is setup on the COLA computers. Here's a few scenarios where that may not work:

* I found a nice example for plotting my data by searching the internet and I tried it, but the Python package in the example is not installed on COLA computers.  
* I found a function in a Python package that does exactly what I need.  It would save me so much time to use it rather than write my own, but the package version on the COLA computers is old and does not have this new function. 
* I want to preserve the exact packages and versions of packages I used in my data analysis so that others can use my codes or so I can reproduce all my analysis when my paper comes back from review.

In this lesson we will learn how to setup our own Python environment so that we can control what packages and versions are available to our programs.
