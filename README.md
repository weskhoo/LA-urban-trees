# LA-urban-trees
Urban forests can provide environmental, economic and social benefits. Here, statistical analyses were done to understand the relationship between Los Angeles Urban Trees and environmental, economic and social indicators. Prior to final analysis, the data obtained was cleaned and explored. 

# Importing Data

1. LA county data on urban trees were imported from https://github.com/stiles/data/tree/master/los-angeles-street-trees
2. LA county data on median income, federal poverty levels, indices of enviromental justice (i.e. hazard proximity to sensitive uses, health risk and exposure, social and health vulnerability, and climate change vulnerability) were imported from https://geohub.lacity.org/search

# Cleaning Data

1. Urban trees Data (Starting with 1.7 Million Trees)
  i. Removing counties dataset which has inaccurate geometry information. (49K Trees)
  ii. Removing columns with 100% missing values.
  ii. Removing rows where a tree information represents a vacant site.
  iii. Cleaning botanical names of trees.
  iv. Cleaning tree geometry information. (Ending with 1.4 Million Trees)
  
2. Median income data
  i. Removing rows with no median income data.
  ii. Cleaning location data to match with main dataset.
  
3. Federal poverty data
  i. Calculating 100% federal poverty level (FPL) and 200% FPL data from population data.
  ii. Cleaning location data to match with main dataset.
  
4. Environmental justice data
  i. Cleaning location data to match with main dataset.
  
# Preparing Data
1. Calculate trees/unit area according to boundaries set by US Cenus Tract. 

# Data Exploration

1. Urban tree densities by US Cenus Tract boundaries.

<img src="https://user-images.githubusercontent.com/70302224/98636877-81c12380-22dc-11eb-927d-03d631a695b9.png" width="400" height="600"/>
* The percent of students (total of 11th and 12th Graders) who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math.
