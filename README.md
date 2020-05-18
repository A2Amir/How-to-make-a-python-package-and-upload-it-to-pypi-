# How to make a python pakage and upload it to pypi 
## A. Make a python pakage 
### 1. First modular(separating code into different files) your codes.
### 2. A Python package also needs an __init__.py file. In this [example](https://github.com/A2Amir/How-to-make-a-python-pakage-and-upload-it-to-pypi-/tree/master/Package/Gaussian_Bionomial_Distributions), you can see how modularized codes look like and how to create this __init__.py file

### 3. Inside [the python package folder](https://github.com/A2Amir/How-to-make-a-python-pakage-and-upload-it-to-pypi-/tree/master/Package), you'll need to create a few files:

* A **setup.py** file, which is required in order to use pip install
* A folder name, for me called **'Gaussian_Bionomial_Distributions'**, which is the name of the Python package and inside it are modularized codes and an **__init__.py** file. see this [example](https://github.com/A2Amir/How-to-make-a-python-pakage-and-upload-it-to-pypi-/tree/master/Package/Gaussian_Bionomial_Distributions).

### 3. In the python package directory you can use this command ***{pip install .}*** to install the package into your local Python installation.

 * Notice if you create a conda environment, activate the environment, and then use this command {pip install .} to install the distributions package, you'll find that the system installs your package [globally rather than in your local conda environment](https://github.com/ContinuumIO/anaconda-issues/issues/1429). However, if you create the conda environment and install pip simultaneously, you'll find that pip behaves as expected installing packages into your local environment
 
### 4. If everything is set up correctly, pip will install the distributions package into the workspace. You can then start the python interpreter from the terminal typing: 
   
   * python
   * Then within the Python interpreter, you can use the distributions package like from my package
   ~~~python
   
   from Gaussian_Bionomial_Distributions import Gaussian
     
   ~~~
     
## B. Putting Code on PyPi

### PyPi vs. Test PyPi:
* Note that [pypi.org](https://pypi.org) and [test.pypy.org](https://test.pypi.org) are two different websites. You'll need to register separately at each website. If you only register at pypi.org, you will not be able to upload to the test.pypy.org repository.Also, remember that your package name must be unique. If you use a package name that is already taken, you will get an error when trying to upload the package.

* Remember that your package name must be unique. If you use a package name that is already taken, you will get an error when trying to upload the package.

### Summary of the Terminal Commands Used


* You'll need to create a **setup.cfg** file, **README.md file**, and **license.txt** file. You'll also need to create accounts for the pypi test repository and pypi repository. Don't forget to keep your passwords; you'll need to type them into the command line.

* Once you have all the files set up correctly, you can use the following commands on the command line (note that you need to make the name of the package unique, for example the change of the name of my package from Gaussian_Bionomial_Distributions to something else. That means changing the information in setup.py and the folder name):

* cd to setup.py directory(for example here cd Package).
* Run **python setup.py sdist**
* Run **pip install twine**

### commands to upload to the pypi test repository
* twine upload --repository-url https://test.pypi.org/legacy/ dist/*
* pip install --index-url https://test.pypi.org/simple/ Gaussian_Bionomial_Distributions

### command to upload to the pypi repository
* twine upload dist/*

### command to install the uploaded package from the pypi repository
* pip install Gaussian_Bionomial_Distributions
