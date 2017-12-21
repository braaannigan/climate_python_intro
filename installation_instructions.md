---
layout: default
visible: 1
---

# Python installation
Python may be installed on your system already.  However, we will be using the Anaconda distribution of python.  To get this, you go to the page below (changing the operating system if necessary) and download the **python 3** version.

https://www.anaconda.com/download/

The anaconda installer may ask your permission to do various things such as appending to your .bashrc file during installation.  You can agree to all the points it asks.

All of the commands listed below occur in the terminal (mac/unix) or the Anaconda prompt (windows),
rather than inside python.

For mac/linux you need to start a new terminal session (mac/linux) once Anaconda is installed.
Enter
```
conda info
```
to check that conda is available.

In windows you need to run all commands in the Anaconda
prompt (search for Anaconda from the Start menu).

# Virtual environment
It is good programming practice to create 'virtual environments' on your
machine.  A virtual environment is like a 'walled-off' installation of a
 program on your machine.  Using a virtual environment lets you play around
 with different installation set-ups on the same machine (similar to
  having different versions of matlab on the same machine).

For this workshop, we will create a virtual environment called 'work3' that has the packages that we need for the workshop installed.

You can create this environment using the conda virtual environment manager by running the following command
in the terminal (mac/linux) or the Anaconda prompt (windows):
```
conda create -n work3 python=3.6.1 ipython jupyter scipy numba xarray dask holoviews bokeh seaborn
```

This command 1) creates an environment called 'work3', 2) sets python 3.6.1 as the
python version and then 3) installs the packages listed from ipython:seaborn.  

You can then 'activate' (switch-to) this virtual environment with the command:
```
source activate work3
```
or in windows

```
activate work3
```

You should see 'work3' now appearing at the start of the command prompt.

**You need to activate the work3 environment when you load the jupyter notebooks.**

You can deactivate and return to your root environment with the command:
```
source deactivate work3
```
or in windows:
```
deactivate work3
```

# ipython kernel
We will be using interactive jupyter notebooks in the workshop.  
You can make sure that the notebook sees the python installation in the ```work3``` virtual environment.  
You do this with the command
```
python -m ipykernel install --user --name work3 --display-name "work3"
```

# Tutorial materials
Once you have your virtual environment set up, you can download the tutorial
materials.  

## Downloading the materials
In your browser, go to this page:
https://github.com/braaannigan/climate_python_intro
and click on the green clone or download button.

If you want to use git then you can simply clone the repository
to the current directory in the command line by running:
```
git clone https://github.com/braaannigan/climate_python_intro.git
```

If you don't want to use git, then you can download the material.  First,
create a directory called ```climate_python_intro``` for the workshop material.

If you are using mac or linux:
   click the 'copy to clipboard' button on the pop-up box on the website to copy the address;
   Navigate to your workshop directory in the terminal.  
   and in your terminal run the command
   git clone <paste address>

If git clone doesn't work then follow the windows instructions below.

If you are using windows:
    Click on the green clone or download button.
    Click on "download zip" at the bottom of the pop-up box.  Unzip the file into your workshop directory

## Opening the materials
Once you have cloned/downloaded the materials, you can open them.
Navigate to your new ```climate_python_intro``` directory.  
Open a jupyter notebook in that directory by running
```
jupyter notebook
```
in the command line.  If you are asked to specify a kernel, make sure that
you choose ```work3```.  Check that you can open the pandas_1.ipynb file and do the first import statements.
If you have problems and google can't solve them, then let me know.
