

### Table of Contents

1. [Installation](#installation)
3. [File Descriptions](#files)
2. [Use Process](#motivation)
4. [Author](#licensing)

# 1. Installation <a name="installation"></a>

To install via Repo , download the Repository and use the command below, it will automatically install  the package coded in this Repo.

		pip install .
Or use the command below to downlaod the uploaded package from [my pypi account](https://pypi.org/manage/projects/)

		pip install Gaussian_Bionomial_Distributions
        
# 2. File Descriptions <a name="files"></a>

Links to the corresponding codes, which are stored in the [Code](https://github.com/A2Amir/How-to-make-a-python-package-and-upload-it-to-pypi-/tree/master/Package/Gaussian_Bionomial_Distributions) folder.

# 3. Use Process <a name="motivation"></a>

The process uses to create Bionomial, Distribution Gaussians for adding and representing them.

      from Gaussian_Bionomial_Distributions import Gaussian
      from Gaussian_Bionomial_Distributions import Binomial

      gaussian = Gaussian(25, 2)

      
      gaussian.calculate_mean()
      gaussian.calculate_stdev()
      gaussian.pdf(25)
    
      gaussian.mean
      gaussian.stdev
      
      gaussian_one = Gaussian(25, 3)
      gaussian_two = Gaussian(30, 4)
      gaussian_sum = gaussian_one + gaussian_two
      
      
      
      binomial = Binomial(0.4, 20)
      binomial.calculate_mean()
      binomial.calculate_stdev()
      
      binomial.p
      binomial.n
      binomial.pdf(5)
      
      
      binomial_one = Binomial(.4, 20)
      binomial_two = Binomial(.4, 60)
      binomial_sum = binomial_one + binomial_two
      
# 5. Author <a name="licensing"></a>
	Copyright (c) 200 Amir-Ziaee 
