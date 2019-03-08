# Understanding Self-Driving Cars 
This repository contains code exercises and materials for sdc-study jam program. It consists of tutorial notebooks that demonstrate, or challenge you to complete, various applications and techniques. These notebooks depend on a number of software packages to run, and so, we suggest that you create a local environment with these dependencies by following the instructions below.

# Configure and Manage Your Environment with Anaconda

Per the Anaconda [docs](https://www.anaconda.com/documentation-page/):

> Conda is an open source package management system and environment management system 
for installing multiple versions of software packages and their dependencies and 
switching easily between them. It works on Linux, OS X and Windows, and was created 
for Python programs but can package and distribute any software.

## Overview
Using Anaconda consists of the following:

1. Install [`anaconda`](https://www.anaconda.com/distribution/) on your computer, by selecting the latest Python version for your operating system. If you already have `conda` or `miniconda` installed, you should be able to skip this step and move on to step 2.
2. Create and activate * a new `conda` [environment](https://docs.anaconda.com/anaconda/navigator/tutorials/manage-environments/).

\* Each time you wish to work on any exercises, activate your `conda` environment!

## 1. Installation

**Download** the latest version of `anaconda` that matches your system.

|        | Linux | Mac | Windows | 
|--------|-------|-----|---------|
| 64-bit | [64-bit (bash installer)][lin64] | [64-bit (bash installer)][mac64] | [64-bit (exe installer)][win64]
| 32-bit | [32-bit (bash installer)][lin32] |  | [32-bit (exe installer)][win32]

[win64]: https://repo.anaconda.com/archive/Anaconda3-2018.12-Windows-x86_64.exe
[win32]: https://repo.anaconda.com/archive/Anaconda3-2018.12-Windows-x86.exe
[mac64]: https://repo.anaconda.com/archive/Anaconda3-2018.12-MacOSX-x86_64.sh
[lin64]: https://repo.anaconda.com/archive/Anaconda3-2018.12-Linux-x86_64.sh
[lin32]: https://repo.anaconda.com/archive/Anaconda3-2018.12-Linux-x86.sh

## 2. Create and Activate the Environment

For Windows users, these following commands need to be executed from the **Anaconda prompt** as opposed to a Windows terminal window. For Mac, a normal terminal window will work. 

#### Git and version control
These instructions also assume you have `git` installed for working with Github from a terminal window, but if you do not, you can download that first with the command:
```
conda install git
```

**Now, we're ready to create our local environment!**

1. Clone the repository, and navigate to the downloaded folder. This may take a minute or two.
```
git clone https://github.com/fnplus/sdc-studyjam.git
cd sdc-studyjam
```

2. Create (and activate) a new environment, named `sdc-fnplus` with Python 3.6. If prompted to proceed with the install `(Proceed [y]/n)` type y.

	- __Linux__ or __Mac__: 
	```
	conda create -n sdc-fnplus python=3.6
	source activate sdc-fnplus
	```
	- __Windows__: 
	```
	conda create --name sdc-fnplus python=3.6 
	or
	conda create -n yourenvname python=x.x anaconda
	conda activate sdc-fnplus
	```
3. Install a few required pip packages, which are specified in the requirements text file (including OpenCV).
    ```
    pip install -r requirements.txt
    ```
    > For Installing in anaconda env, follow the instruction in specific folder 

4. That's it!

To exit the environment when you have completed your work session, simply close the terminal window. OR
```
conda deactivate sdc-fnplus
```


### Notes on environment creation and deletion

**Verify** that the `sdc-fnplus` environment was created in your environments:

```
conda info --envs
```

**Cleanup** downloaded libraries (remove tarballs, zip files, etc):

```
conda clean -tp
```

**Uninstall** the environment (if you want); you can remove it by name:

```
conda env remove -n sdc-fnplus
```
