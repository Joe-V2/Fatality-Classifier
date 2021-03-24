# Fatality Classifier
## Description
Python, Pandas and Scikit-Learn packages automate all taxonomy, cleaning, modelling, and training - all across 3 different classification methods. Enhanced with the ADA-boosted equivalents of each one used, this script produces comparative performance statistics based on sensitivity, specificity, and euclidean/manhattan metrics to define the comparative success of each one. To run it yourself, use the .csv file, or populate your own using the format specified in its headings.  

## How do I use this?
This file is configured to work with Jupyter Notebook, or anything that can run a .ipnyb file. Read the markdown cells within it for a step-by-step breakdown of how it works, and consult the resultant CSV files from its output for the results of the experiment.  
It is designed as an automated process from start to finish, such that not only is it deployable on any data that matches the same basic taxonomy, but also operates free from user supervision (although a certain degree of oversight is greatly encouraged).  

## What does it do?

The pipeline is designed to do the following:

1. Read in data from HeartData.csv, and provide a taxonomic overview.
2. Remove, and store elsewhere, any exact duplicates to prevent overtraining, as well as enforce taxonomic rules for feature data types to insulate against data error.
3. Remove elements with outlying features from the cleaned dataset, in both class-specific and global contexts, using boundaries defined against the standard deviations of the means in either, to isolate against outliers influencing regressional outcomes.
4. Transform nominal and numeric data types to numeric and nominal equivalents respectively, polarising any binary types in the process, and storing the unanimously typed resultant dataframes in one container per type. Also insulates against zero-division error.
5. Classifies all resultant dataframes against multiple classifiers using several parameter configurations:
  * Decision trees, for their excellent visualisation capacity for how classifications are made
  * KMeans, for a comparison of dimensional clustering against multifeatured algorithmical classification
  * Multi-Layer Perceptron network, for a comparison of novel classification technique against various data types
  * ADA-Boosted decision tree, for a comparison of the benefits of meta-analysis in algorithmic bounds classification
  * Bagged KMeans, for a comparison of the benefits of meta-analysis in clustered spatial classification
  
This process produces performance metrics for all specified classifiers, rooted in the sensitivity and specificity given by their respective error matrices. These are plotted on a two-feature point graph as a distance away from the perfect, always-right ideal model, by first converting accuracy into two percentage with regards to both positive and negative error, and then using these as the x and y coordinates for a manhattan or euclidean distance away from the perfect origin.

Try it for yourself, make your own data, try and confuse it, whatever you do - just have fun!
