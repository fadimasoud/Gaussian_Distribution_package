dsnd_probabilit_Fadi folder contain two class

First Class:
Generic distribution class for calculating and visualizing a probability distribution.
		class Distribution:
        Attributes:
            mean (float) representing the mean value of the distribution
            stdev (float) representing the standard deviation of the distribution
            data_list (list of floats) a list of floats extracted from the data file
       Method:
       		- read_data_file:
            Function to read in data from a txt file. The txt file should have 
            one number (float) per line. The numbers are stored in the data attribute.                
            Args:
                file_name (string): name of a file to read from        
            Returns:
                None

==========

Second Class:
Gaussian distribution class for calculating and visualizing a Gaussian distribution.
	class Gaussian(Distribution):
    Attributes:
        mean (float) representing the mean value of the distribution
        stdev (float) representing the standard deviation of the distribution
        data_list (list of floats) a list of floats extracted from the data file
    Method:
    	- calculate_mean:
	    	Method to calculate the mean of the data set.        
    	    Args: 
        	    None        
        	Returns: 
            	float: mean of the data set        
        - calculate_stdev:
        	Method to calculate the standard deviation of the data set.        
            Args: 
                sample (bool): whether the data represents a sample or population
            Returns: 
                float: standard deviation of the data set
       	- read_data_file:
        	Method to read in data from a txt file. The txt file should have one 
            number (float) per line. The numbers are stored in the data attribute. 
            After reading in the file, the mean and standard deviation are calculated
            Args:
                file_name (string): name of a file to read from
            Returns:
                None
        - plot_histogram:
        	Function to output a histogram of the instance variable data using 
            matplotlib pyplot library.
            Args:
                None
            Returns:
                None
        - pdf:
        	Probability density function calculator for the gaussian distribution.		
            Args:
                x (float): point for calculating the probability density function
            Returns:
                float: probability density function output
       - plot_histogram_pdf:
           Function to plot the normalized histogram of the data and a plot of the 
           probability density function along the same range
            Args:
                n_spaces (int): number of data points 
            Returns:
                list: x values for the pdf plot
                list: y values for the pdf plot
       - __add__:
           Function to add together two Gaussian distributions
            Args:
                other (Gaussian): Gaussian instance
            Returns:
                Gaussian: Gaussian distribution
       - __repr__:
             Function to output the characteristics of the Gaussian instance
              Args:
                  None
              Returns:
                  string: characteristics of the Gaussian

==========

Third Class:
Binomial distribution class for calculating and visualizing a Binomial distribution.
	class Binomial(Distribution)    
    Attributes:
        mean (float) representing the mean value of the distribution
        stdev (float) representing the standard deviation of the distribution
        data_list (list of floats) a list of floats to be extracted from the data file
        p (float) representing the probability of an event occurring
        n (int) the total number of trials
   Method:
   		- calculate_mean:
            Function to calculate the mean from p and n        
            Args: 
                None        
            Returns: 
                float: mean of the data set
        - calculate_stdev:
            Function to calculate the standard deviation from p and n.
            Args: 
                None        
            Returns: 
                float: standard deviation of the data set
       - replace_stats_with_data:
           Function to calculate p and n from the data set        
            Args: 
                None        
            Returns: 
                float: the p value
                float: the n value
      - plot_bar:
          Function to output a histogram of the instance variable data using 
          matplotlib pyplot library.        
            Args:
                None            
            Returns:
                None
      - pdf:
          Probability density function calculator for the gaussian distribution.        
            Args:
                k (float): point for calculating the probability density function
            Returns:
                float: probability density function output
      - plot_bar_pdf:
          Function to plot the pdf of the binomial distribution        
            Args:
                None        
            Returns:
                list: x values for the pdf plot
                list: y values for the pdf plot
      - __add__:
          Function to add together two Binomial distributions with equal p        
            Args:
                other (Binomial): Binomial instance            
            Returns:
                Binomial: Binomial distribution
      - __repr__:
          Function to output the characteristics of the Binomial instance.        
            Args:
                None        
            Returns:
                string: characteristics of the Gaussian
                
========
        


