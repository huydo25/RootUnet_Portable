User Guide

### 1. Set up environment and install required package

All the programs are written in Python and used all Python's modules. For user, we recommend using a virtual enviroment(virtualenv, anaconda, etc.) to run the program, which is very convenient in term of setup (or remove) Python's modules. 

In this case, we used Anaconda for Python 3.6. If you haven'y got Anaconda in your system, please download [Anaconda](https://www.anaconda.com/download/) abd install following the typical instruction. 

For Linux:

Run the script to install Anaconda:
```
bash Anaconda3-5.3.0-Linux-x86_64.sh 
```
Note: After anaconda installer complete, please add the script of anaconda to the bashrc and logout.Re-login and check conda works by running `conda`

Next, create a new environment on your system
```
conda create -n my_env
```
This command will create a empty environment for you, and you can install any package you want. However, we recommended to create a new enviroment with all conda default packages.
```
conda create -n my_env python=3 anaconda=4
```
After that, to activate your enviroment, run
```
source activate my_env
```
To see all the packages have been installed in Anaconda, run:
```
conda list
```
All the required package has been list in requirement.txt, please install it following the order in the list.

To install a package in anaconda, please run:
```
conda install package_name
```
Note: pip is also avaiable in Anaconda, if you do not familiar with Anaconda, using pip is another choice.  

For Windows:

Updating

For MacOSX:

Updating

Note: If your device contains GPU, you can set up a conda environment for GPU to accelarate the computing process.

### 2.Running the program
1. Put all the image into the input/ directory
2. Run script to import pre-trained model and predict output
```
python runme.py
```
3. Wait until process completed. Please check the output in the /output directory

### 3. Optional

Updating
