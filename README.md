# Project-Airbnb-price-prediction
SUMMARY 

# Project Rationale

⚇ The Airbnb platform has revolutionised the way people travel and find accommodation. 

⚇ But with a growing popularity, hosts face the challenge of setting competitive prices to attract guests. 

**This project aims to pin point the most impostant factors that drive Airbnb price evolution.**

# Research Question

*What factors impact the most significantly Airbnb listings prices in major European cities ?*

5 criteria 

**Price** : How much is the listing per night ?

**Location** : Where is the listing located?

**Guest Rating** : What did guest say about their stay ?

**Listing type** : What is the size of the listing? Is it shared with other guests?

**Proximity to activities** : How far are important attractions ?

Which leaves us with a price variable as independent and predictors variables.

# Exploring the Dataset

## **Data Collection**

Using the Kaggle dataset “Airbnb listing” uploaded in 2016. Exploring it as CSV file ready for data manipulation in Stata

## **Data Cleaning**

The data set does not countain any NAs. Check for duplicate or incoherent data entries.

## **Descriptive Statistics**

We summarise the dataset using basic statistical measures. Examine the distribution of the target variable (price). Explore the distributions of other relevant variables.

**Table 1** : Dataset Descriptive Summary

![Stata%20Describe%20Airbnb](https://github.com/user-attachments/assets/6acbe910-a9dc-446d-9667-f4048f95bd7c)


**Table 2** : Descriptive table of relevant variables

<img width="537" alt="image-2" src="https://github.com/user-attachments/assets/41c4cd49-4ebc-440b-ba61-d1a32c4897c7" />




**Table 3 :** Variables Frequency 

<img width="648" alt="image-3" src="https://github.com/user-attachments/assets/4f69d9c4-65dc-45b6-a39d-933386c40b4b" />
<img width="639" alt="image-4" src="https://github.com/user-attachments/assets/5dab3f17-0c1d-4d96-9794-4fe71ec6cfec" />
<img width="639" alt="image-5" src="https://github.com/user-attachments/assets/024206a1-a550-42d3-af08-a6a5e2aa5fa2" />






Let’s perform a first regression

</aside>

**Table 4** : Performance results of a first regression with continuous price variable as the independent.

*price = β0 + β1×citycenterkm + β2×metrodistancekm + β3×cleanlinessrating + β4×guestsatisfaction + β5×superh + β6×multiplerooms + β7×private + β8×attraction + β9×restaurant*

<img width="1168" alt="image-6" src="https://github.com/user-attachments/assets/639bfdd2-f146-44bc-b50c-f5f1dbe0a1af" />


<aside>


Independent Price Variable 

</aside>

**Figure 1** : Kernel Density Estimate with price as a continuous variable
<img width="675" alt="image-7" src="https://github.com/user-attachments/assets/e700c3f5-b1d7-43a8-bb86-f22adac85340" />

**Figure 2** : Kernel Density Estimate with price as a logarithmic variable
<img width="671" alt="image-8" src="https://github.com/user-attachments/assets/a80cf1ab-3f2b-484b-a07a-8eb296eeff3d" />

<aside>


Distribution of Price Indicators


</aside>

**Figure 3** : Distribution of Price 

<img width="1056" alt="image-9" src="https://github.com/user-attachments/assets/8cc9a440-a506-4e7f-b93b-1b0040c5f513" />



<aside>


Distribution of Location Predictors 

</aside>



**Figure 4** : City Frequency 

<img width="575" alt="image-10" src="https://github.com/user-attachments/assets/a2cc20a0-a4a6-4307-9bc1-c68b799de358" />





**Figure 5**: Location Indicators 

<img width="789" alt="image-11" src="https://github.com/user-attachments/assets/e4ec9c8b-0d41-44af-8de2-e333bd08a312" />



➡️

Distribution of Guest Ratings 

</aside>

<aside>
➡️

Distribution of Guest Ratings 

</aside>

**Figure 6** : Boxplots of cleanliness and satisfaction 

<img width="984" alt="image-12" src="https://github.com/user-attachments/assets/d6784272-d1b2-4053-99e7-474a373ad6c8" />

<aside>

  ➡️

Distribution of Proximity Indicators 

</aside>

**Figure 7 :** Proximity Boxplots 
<img width="1049" alt="image-13" src="https://github.com/user-attachments/assets/bc624d10-d721-4a17-b3b0-92a74d51d809" />



# Model Building  and Analysis

With out clean data we can now perform a regression with the price variable and all predictors.

**Table 7**  : Regression Models Fit

<img width="952" alt="image-14" src="https://github.com/user-attachments/assets/2f27e6ec-10b4-4243-b8c4-eefb24fd2bb4" />



Checking that assumptions are met. 


**Residuals and Multicollinearity**

**Figure 8** : Histogram of residuals for logarithmic price model

<img width="860" alt="image-15" src="https://github.com/user-attachments/assets/b27cd2e2-9eb1-4aa7-aba6-3139063f0f23" />

**Table 8** : VIF results  for logarithmic price model

<img width="411" alt="image-16" src="https://github.com/user-attachments/assets/93e7eb3d-d855-47a5-ae61-958343164690" />

**Collinearity**

**Table 9** : Correlation Matrix
<img width="1103" alt="image-17" src="https://github.com/user-attachments/assets/20bfc35c-8b62-434b-ab15-b5cf70ef5e10" />

**Heteroscedasticity**

**Figure 9** : Scatterplot comparing fitted and residual values  for logarithmic price model

<img width="952" alt="image-18" src="https://github.com/user-attachments/assets/f92bfbb2-5230-41bc-bb43-8f4f5633b0ca" />


<aside>
➡️

Final Regression Summary 

</aside>

**Table 10**: Regression Summary for Logaritmic Price

<img width="1070" alt="image-19" src="https://github.com/user-attachments/assets/b6625af3-83f2-498d-9177-a997de3c8f3c" />


**Table 11** : Models performance for each european cities
<img width="1060" alt="image-20" src="https://github.com/user-attachments/assets/6b2f68cd-3247-4fa8-97ba-6930c8052b07" />


**Table 12** : Regression Summary for top three performing models
<img width="567" alt="image-21" src="https://github.com/user-attachments/assets/b2c23a9b-af2f-4c3f-9f98-0e54a2565676" />
<img width="567" alt="image-22" src="https://github.com/user-attachments/assets/6779b0eb-3239-4bfd-b547-188ff30f1438" />


# Conclusion and Recommendations


Most Expensive City by average price in euro

<img width="566" alt="image-23" src="https://github.com/user-attachments/assets/f80e7a25-3462-4224-95af-83b429303f4a" />


Most Affordable City by average price in euro 


<img width="603" alt="image-24" src="https://github.com/user-attachments/assets/abb587b9-b950-457e-8f30-3f931edd209e" />
<img width="512" alt="image-25" src="https://github.com/user-attachments/assets/8ed72e76-86d4-4658-b844-c1a3d2543574" />
<img width="507" alt="image-26" src="https://github.com/user-attachments/assets/6b287620-fc33-41ca-b1cd-28a77aa8fa32" />


### Answering the research question according to our findings

*What factors impact the most Airbnb listings prices in major European cities ?*



Most significant across all cities 

<img width="1314" alt="image" src="https://github.com/user-attachments/assets/7eaf4252-d76d-4ca5-b68e-48d31022ce6a" />



Most significants factors in Rome, Barcelona and Lisbon 
<img width="1292" alt="image-27" src="https://github.com/user-attachments/assets/c715fe7d-2df9-4f6a-ae91-39aefc5bf6b8" />


