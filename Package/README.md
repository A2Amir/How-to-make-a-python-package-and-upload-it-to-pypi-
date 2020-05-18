

### Table of Contents

1. [Installation](#installation)
3. [File Descriptions](#files)
2. [Using Process](#motivation)
4. [Author](#licensing)

# 1. Installation <a name="installation"></a>

To install via pip , use the command below, it will automatically install all the liberary used in this Repo.

		pip install 
        
        
# 2. File Descriptions <a name="files"></a>

Links to the corresponding codes, which are stored in the [Code]() folder.

# 3. Data Science Process <a name="motivation"></a>

The process uses to create Bionomial, Distribution Gaussians for adding and representing them.

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