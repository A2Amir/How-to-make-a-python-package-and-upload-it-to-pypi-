# How to make a python pakage and upload it to pypi 
## A. Make a python pakage 
### 1. First modular(separating code into different files) your codes.
### 2. A Python package also needs an __init__.py file. In this [example](https://github.com/A2Amir/How-to-make-a-python-pakage-and-upload-it-to-pypi-/tree/master/Package/Gaussian_Bionomial_Distributions), you can see how modularized codes look like and how to create this __init__.py file

### 3. Inside [the python package folder](https://github.com/A2Amir/How-to-make-a-python-pakage-and-upload-it-to-pypi-/tree/master/Package), you'll need to create a few files:

* A **setup.py** file, which is required in order to use pip install
* A folder name, for me called **'Gaussian_Bionomial_Distributions'**, which is the name of the Python package and inside it are modularized codes and an **__init__.py** file. see this [example](https://github.com/A2Amir/How-to-make-a-python-pakage-and-upload-it-to-pypi-/tree/master/Package/Gaussian_Bionomial_Distributions).

### 3. In [the python package folder](https://github.com/A2Amir/How-to-make-a-python-pakage-and-upload-it-to-pypi-/tree/master/Package) you can use this command ***{pip install .}*** to install the package into your local Python installation.

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

## More PyPi Resources
This link has a good tutorial on distributing Python packages including more configuration options for your **setup.py** file: [tutorial on distributing packages](https://packaging.python.org/tutorials/distributing-packages/). You'll notice that the python command to run the setup.py is slightly different with 

    python3 setup.py sdist bdist_wheel
   
This command will still output a folder called **dist**. The difference is that you will get both a **.tar.gz** file and a **.whl** file. The **.tar.gz** file is called a source archive whereas the **.whl** file is a built distribution. The **.whl** file is a newer type of installation file for Python packages. When you pip install a package, pip will first look for a whl file (wheel file) and if there isn't one, will then look for the tar.gz file. 

A tar.gz file, ie an sdist, contains the files needed to [compile](https://en.wikipedia.org/wiki/Compiler) and install a Python package. A whl file, ie a built distribution, only needs to be copied to the proper place for installation. Behind the scenes, pip installing a whl file has fewer steps than a tar.gz file.

###  For a much more detailed explanation of distributing Python packages, check out the documentation on Distutils. 
1.	[Introduction](https://docs.python.org/3/distutils/introduction.html)
2.	[setup.py script](https://docs.python.org/3/distutils/setupscript.html)
3.	[config file](https://docs.python.org/3/distutils/configfile.html)
4.	[source distributions](https://docs.python.org/3/distutils/sourcedist.html)
5.	[built distributions](https://docs.python.org/3/distutils/builtdist.html)
6.	[uploading to PyPi](https://docs.python.org/3/distutils/packageindex.html)

