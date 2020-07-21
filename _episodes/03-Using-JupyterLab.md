---
title: "Using JupyterLab"
teaching: 5
exercises: 0
questions:
- "How do I run Python programs in JupyterLab?"
- "What else is useful in JupyterLab?"
objectives:
- "TEST"
keypoints:
- "JupyterLab is an interactive Python interface that is ideal for scientific work"
---

## Run an existing Jupyter notebook in JupyterLab? 

Get some files needed for this and future lessons.

~~~
$ git clone XXXX
~~~
{: .language-bash}

Login to a COLA computer
Change directories to XXXXX

Launch Jupyter on a COLA computer:

~~~
$ jupyter lab --no-browser --ip=`hostname` --port=8878
~~~
{: .language-bash}

Login to COLA for JupyterLab

~~~
$ ssh -N -L 8878:colaX.gmu.edu:8878 <YOURUSERNAME>@colaX.gmu.edu
~~~
{: .language-bash}

Open a web browser to the following location: http://localhost:8878

Take a look at the left side of the JupyterLab interface.  It shows the files located in the directory you launched in from. 
Jupyter notebooks have the file extension `.ipynb`. We will open the notbook `XXXX.ipynb` by clicking on it in the left side of JupyterLab.

The notebook contains separate `cells`. Some cells contain Python code, some contain text, and some contain Markdown. 

We can run all the cells to run our program:
Click `Run`->`Run All Cells` 

We can run individual cells to see what happens when we execute a specific block of code:
Click in the first code cell.
Click the arrow.
Click the arrow again.

What happens?

Click in a Text cell.
Click the arrow.

What happens?

Click in a Markdown cell.
Click the arrow.

What happens?

> ## What is a Markdown cell?
>
> Markdown is a text formatting language.
>
{: .callout}

Create a new code cell and add the following lines of code:

~~~
x=1
y=2
z=x+y
~~~
{: .language-python}

Run the cell and see what happens.

Create a new Markdown cell above the code cell and add the following lines:

~~~
Test Code
# Test Code
## Test Code
### Test Code
*Test Code*
`Test Code`
~~~
{: .source}

Run the cell and see what happens.

Save your notebook using the `Save`->`Save Notebook As...` menu option. 


