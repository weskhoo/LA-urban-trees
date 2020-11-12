# Los Angeles urban trees and their association to social and economic status.
Urban forests can provide environmental, economic and social benefits. Here, statistical analyses were done to understand the relationship between Los Angeles Urban Trees and environmental, economic and social indicators. Prior to final analysis, the data obtained was cleaned and explored. 
The work was completed in three notebooks:

* [Data Wrangling (Part 1)](https://github.com/weskhoo/LA-urban-trees/blob/main/Data_Wrangling_Part_1.ipynb)

* [Data Wrangling (Part 2)](https://github.com/weskhoo/LA-urban-trees/blob/main/Data_Wrangling_Part_2.ipynb)

* [Data Wrangling (Part 3) & Data Analysis](https://github.com/weskhoo/LA-urban-trees/blob/main/Data_Wrangling_Part_3_and_Data_Analysis.ipynb)

# Importing Data

1. LA county data on urban trees were imported from https://github.com/stiles/data/tree/master/los-angeles-street-trees
2. LA county data on median income, federal poverty levels, indices of enviromental justice (i.e. hazard proximity to sensitive uses, health risk and exposure, social and health vulnerability, and climate change vulnerability) were imported from https://geohub.lacity.org/search

# Cleaning Data

1. Urban trees Data (Starting with 1.7 Million Trees)

    * Removing counties dataset which has inaccurate geometry information. (49K Trees)
    
    * Removing columns with 100% missing values.
    
    * Removing rows where a tree information represents a vacant site.
    
    * Cleaning botanical names of trees.
    
    * Cleaning tree geometry information. (Ending with 1.4 Million Trees)
  
2. Median income data

    * Removing rows with no median income data.
    
    * Removing data from median income data > $150K. These boundaries are in areas that have close access to natural forestry. 
    
    * Cleaning location data to match with main dataset.
  
3. Federal poverty data

    * Calculating 100% federal poverty level (FPL) and 200% FPL data from population data.
    
    * Cleaning location data to match with main dataset.
  
4. Environmental justice data

    * Cleaning location data to match with main dataset.
  
# Preparing Data
1. Calculate trees/unit area according to boundaries set by US Cenus Tract. 

# Data Exploration

1. **Urban tree densities by US Cenus Tract boundaries.**
<img src="https://user-images.githubusercontent.com/70302224/98636877-81c12380-22dc-11eb-927d-03d631a695b9.png" width="400" height="500"/>

* Tree densities appear to follow a similar trend to median income within boundaries. (Median income plot not shown)

2. **Median income and 100% federal poverty level by US Cenus Tract boundaries.**
<img src="https://user-images.githubusercontent.com/70302224/98899484-78fb5980-2464-11eb-899c-4d491ce664be.png" width="600" height="400"/>

* Similar trend to between these 2 datasets (median income, 100% FPL). 

* High median income areas such as Rolling Hills Estate, Beverly Glen, Hollywood Hills, Bel Air, have low poverty rates. 

* Low median income areas are found close to downtown LA, have up higher poverty rates.

3. **Pairplot of tree density, median incomeand 100% federal poverty level (FPL) rates.**
<img src="https://user-images.githubusercontent.com/70302224/98899350-42254380-2464-11eb-9c7c-8d00437a2974.png" width="400" height="400"/>

* Tree density data is heavily skewed to the right.

* Possible positive association between median income and 100% FPL rates.

* Possible negative association between tree densities and 100% FPL rates.

4. **Environmental Justice Indices by US Cenus Tract boundaries.**
<img src="https://user-images.githubusercontent.com/70302224/98899607-b9f36e00-2464-11eb-8f74-f115ea40a8b1.png" width="700" height="400"/>

* Explanation for the scores can be found here (https://planning.lacounty.gov/assets/img/gis/agol/Green_Zones_EJSM_Data_Sources.pdf).

* Similarly, all 4 indices for environmental justice shows high scores around DTLA area, with the exception of Climate Change score which is also high around the northen part of LA county.

5. **Matrix Correlation plot of median income, 100% federal poverty level (FPL) rates, density and environmental justice indices.**
<img src="https://user-images.githubusercontent.com/70302224/98899294-2de14680-2464-11eb-9bc8-0f20c0cc9008.png" width="500" height="400"/>

* HazScore: hazard proximity to sensitive uses; HealthScore: health risk and exposure; SVscore: social and health vulnerability; CCVscore: climate change vulnerability

* Information on environmental justice indices methodology can be found here (https://planning.lacounty.gov/assets/img/gis/agol/Green_Zones_EJSM_Overview.pdf).

* Regression analysis is conducted to determine statistical difference. 

* Positive correlation between median income vs tree density (p < 0.01).

* Negative correlation between 100% FLP (p < 0.01), HazScore (p < 0.01), HealthScore (p < 0.01), SVscore (p < 0.01) vs tree density.

* Even though there is a negative correlation between CCVscore vs tree density, it is not statistically significant. 

# Conclusion

* There is an association between median income, poverty rates vs urban tree densities in US Census Tract boundaries in the County of Los Angeles.

* Lower urban tree densities are also associated with increased hazards, health risk and social vulnerability. 

* Academic research have shown that urban forest provide vital social services such as improved mental and physical health, improved quality of life, which can contribute to a reduction in crime.

* Additional analysis on LA urban tree densities vs crime, and or academic performance can be done to understand what other social indications are affected by urban forestry.

* Govt officials can seek to increase access to urban forest as a mean to bridge the social and economic gaps in LA.
