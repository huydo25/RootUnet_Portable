# User Guide

## 1. Set up environment and install required package

All the programs are written in Python and used all Python's modules. For user, we recommend using a virtual enviroment(virtualenv, anaconda, etc.) to run the program, which is very convenient in term of setup (or remove) Python's modules. 

In this case, we used Anaconda for Python 3.6. If you haven't got Anaconda in your system, please download [Anaconda](https://www.anaconda.com/download/) and install following the typical instruction. 

**Note**: If your device contains GPU, you are recommend to set up a conda environment for GPU to accelarate the computing 

### Via Anaconda Navigator

#### For Windows, MacOSx, and Linux:

Once Having Anaconda installed, run Anaconda Navigator and:
* On tab **Environments** from the left-column of the program, choose **Import** at the bottom of the second column, and click on *Import new environment*
* On line of **Specification File**, click on the button in the shape of folder and browse to the folder that you extracted the source code, choose the **root_unet_35.yml** (or **root_unet_35_GPU.yml** if there is GPU available on your device) which contain all the needed package, then click on **Open**.
* Now you can see the new environment named as *root_unet_35*. If there already exists an environment has same name, you have to use another name to continue.
* Click to **Import** to create a virtual environment with all pakcages imported.
* After completed, the new enviroment will be shown in the list of enviroments in the second collums of Anaconda navigator. Choose enviroment, then click on **Play** button and **Open Terminal**. Now you have a terminal in the virtual environment that you just created.

### Via Terminal 
####  Only for Linux and MacOSx (Recommended)

Run the script to install Anaconda:
```
    bash Anaconda3-5.3.0-Linux-x86_64.sh 
```
**Note**: After anaconda installer complete, please add the script of anaconda to the bashrc and logout.Re-login and check conda works by running `conda` command.

Next, create a new environment on your system
```
    conda create -n my_env
```
This command will create a empty environment for you. However, you are recommended to create a new enviroment with all conda default packages.
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
When a package is installed, anaconda will check and install other dependencies package automatically.

**Note**: pip is also avaiable in Anaconda, if you do not familiar with conda, using pip is another choice.  
process.

## 2.Running the program
1. Put all the image into the **/input** directory.
2. Run script to import pre-trained model and predict output.
```
    python run.py
```
3. Wait until process completed. Please check the output in the **/output** directory.

**Note**: If you run program on CPU, it will take minutes per image, depending on your CPU capacity. But if you run program on GPU, it only will take around 10 seconds per image, even shorter. 

## 3. Result


<p align="center">
  <img src="https://github.com/huydo25/RootUnet_Portable/blob/master/input/26_5_12_TB2_30_600001.jpg" width="300"/>
  <img src="https://github.com/huydo25/RootUnet_Portable/blob/master/output/26_5_12_TB2_30_600001_pred.jpg" width=300"/>
</p>
