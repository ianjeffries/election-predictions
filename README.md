# election-predictions

<p align="center">
<img src="https://github.com/ianjeffries/election-predictions/blob/master/images/voting_trends.png" alt="alt text" width="640" height="320">
</p>

## Index 
1. [Summary](https://github.com/ianjeffries/election-predictions#summary)
2. [File Directory](https://github.com/ianjeffries/election-predictions#file-directory)
3. [Language and Packages Used](https://github.com/ianjeffries/election-predictions#language-and-packages-used)
4. [Credits](https://github.com/ianjeffries/election-predictions#credits)
5. [License](https://github.com/ianjeffries/election-predictions#license)

## Summary 
The following project accomplishes two goals:  

  1. Predicting the 2016 US election results by county with supervised machine learning in R.
  2. Mining interesting association rules that relate to demographics and voting preference in R. 
  
Three supervised machine learning models are used to predict election results based on demographics: K-Nearest Neighbor, Decision Trees, and Artificial Neural Networks. The models are compared based on accuracy and precision. 

## File Directory

1. [**data**](https://github.com/ianjeffries/election-predictions/tree/master/data) - contains three data sets used in analysis (taken from kaggle, referenced in the credits):  
  a. county_facts.csv - Demographic breakdown of each county  
  b. county_facts_dictionary.csv - Dictionary to decode variable names in county_facts.csv  
  c. pres16results.csv - Results of the 2016 election by county
     
2. [**images**](https://github.com/ianjeffries/election-predictions/tree/master/images) - contains vizualizations:  
  a. decision_tree.png - Decision tree created from modelling process  
  b. model_comparison.png - Comparison of 3 classification models used  
  c. population_trends.png - Population size by voting preference  
  d. voting_trends.png - Voting trends by top 5 normalized demographics
  
3. [**classification**](https://github.com/ianjeffries/election-predictions/tree/master/classification) - contains classification files that predict election outcome based off demographics:  
  a. classification.Rmd - R Markdown detailing the entire classification process, from data cleaning to model creation.
  b. classification.pdf - PDF that shows R code and the outputted results, for easy viewing.

R Markdown document and PDF that shows code and the results, for easy viewing.
  a. R Markdown detailing the entire classification process, from data cleaning to model creation. - contains R Ma
  
4. [**association_rules**](https://github.com/ianjeffries/election-predictions/tree/master/association_rules) - contains association rules files:  
  a. association_rules.Rmd - R Markdown to mine association rules that relate to demographics and voting preference using R.  
  b. association_rules.pdf - PDF that shows R code and the outputted results, for easy viewing.

## Language and Packages Used

R is used for all model building - in the results R and SAS are compared.  

The following packages are used:
  
  ```
#list of packages used
packages <- c("dplyr", "tidyr", "ggplot2", "class", "rpart", "rpart.plot", "neuralnet", "arules",
              "plyr", "mltools", "arulesViz", "plotly", "RCurl")

#check to see if package is already installed, if not, install
for(p in packages){
  if(!require(p, character.only = TRUE)) {
    install.packages(p)
    library(p, character.only = TRUE)
  } 
}
```

## Credits

1. Would like to thank Ben Hammer for the county_facts.csv and county_facts_dictionary.csv datasets, which were taken off [Kaggle](https://www.kaggle.com/benhamner/2016-us-election/home).
2. Would like to thank Steve Palley for the pres16results.csv dataset, which was taken off [Kaggle](https://www.kaggle.com/stevepalley/2016uspresidentialvotebycounty/home).

## License 

MIT License
Copyright (c) 2019 Ian Jeffries
  
