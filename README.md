# Project-Airbnb-price-prediction
SUMMARY 

# Project Rationale

⚇ The Airbnb platform has revolutionised the way people travel and find accommodation. 

⚇ But with a growing popularity, hosts face the challenge of setting competitive prices to attract guests. 

**This project aims to develop a predictive model for Airbnb prices using data analysis techniques.**

# Research Question

*What factors impact and the most significantly Airbnb listings prices in major European cities ?*

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

![Stata Describe Airbnb.jpg](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/49c582f6-5482-4e43-92e8-30092eb02a56/Stata_Describe_Airbnb.jpg)

**Table 2** : Descriptive table of all the relevant variables and their specificities.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/5dd39b55-7235-4f50-9992-64c470e610d4/image.png)

**Table 3 :** Variables Frequency 

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/9323e3dd-4733-4ba3-a096-3b3fbc7141f7/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/b0e481b0-a241-4966-aa39-4ce8852258d1/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/75975fb9-ce0d-4f60-b1fc-0a1d8b5cc274/image.png)

<aside>
🏘️

Let’s perform a first regression

</aside>

**Table 4** : Performance results of a first regression with continuous price variable as the independent.

*price = β0 + β1×citycenterkm + β2×metrodistancekm + β3×cleanlinessrating + β4×guestsatisfaction + β5×superh + β6×multiplerooms + β7×private + β8×attraction + β9×restaurant*

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/6d291d9c-6eda-4a38-b751-1c2909611e69/image.png)

<aside>
➡️

Independent Price Variable 

</aside>

**Figure 1** : Kernel Density Estimate with price as a continuous variable

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/8dab22ef-3fad-47fa-a746-7cd14db40d57/image.png)

**Figure 2** : Kernel Density Estimate with price as a logarithmic variable

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/0408a414-9576-441d-aaae-37c7c9f4b6b9/image.png)

<aside>
➡️

Distribution of Price Indicators

</aside>

**Figure 3** : Distribution of Price 

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/8a0a2236-cf75-44ec-9d71-5d097ee3db88/image.png)

<aside>
➡️

Distribution of Location Predictors 

</aside>

**Figure 4** : City Frequency 

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/63a28cc8-d5d7-4771-a11c-df3e7c24ccb0/image.png)

**Figure 5**: Location Indicators 

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/7b4ecf54-ee7c-4b36-a339-3413ac8a6d7c/image.png)

<aside>
➡️

Distribution of Guest Ratings 

</aside>

<aside>
➡️

Distribution of Guest Ratings 

</aside>

**Figure 6** : Boxplots of cleanliness and satisfaction 

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/6b8850a3-a236-4e22-8f72-fed192399b22/image.png)

<aside>
➡️

Distribution of Proximity Indicators 

</aside>

**Figure 7 :** Proximity Boxplots 

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/fc5f5d70-11bb-4937-9306-bad8defb6b0b/image.png)

# Model Building  and Analysis

With out clean data we can now perform a regression with the price variable and all predictors.

                **Price Performance            VS        Logarithmic Price Performance**

**Table 7**  : Regression Models Fit

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/73e6b891-b165-4648-b4aa-31dc7a197c9a/image.png)

<aside>
➡️

Checking that assumptions are met. 

</aside>

**Residuals and Multicollinearity**

**Figure 8** : Histogram of residuals for logarithmic price model

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/f4fed1b5-f372-44d6-a4e5-53a33787f651/image.png)

**Table 8** : VIF results  for logarithmic price model

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/9aae32df-6838-4cd1-a7b4-cde3dd6f7bce/image.png)

**Collinearity**

**Table 9** : Correlation Matrix

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/23478fe5-5124-406a-a2f3-c95698e7f10a/image.png)

**Heteroscedasticity**

**Figure 9** : Scatterplot comparing fitted and residual values  for logarithmic price model

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/b81be8e8-e27c-482a-9081-0fd355d6b94b/image.png)

<aside>
➡️

Final Regression Summary 

</aside>

**Table 10**: Regression Summary for Logaritmic Price

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/e25bb9c5-482a-40d5-8393-0abe831cbce3/image.png)

**Table 11** : Models performance for each european cities

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/7753e73b-7f8e-4d53-9c85-f8cb17272fa1/image.png)

**Table 12** : Regression Summary for top three performing models

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/4bf83018-afc8-4813-b4cf-6079d68ded2e/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/95c6ea03-156e-4aa9-9f0a-8251bf708382/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/ac18230a-2815-4387-8881-3023453ffdec/image.png)

# Conclusion and Recommendations

<aside>
💸

Most Expensive City by average price in euro

</aside>

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/e95fb6fe-920e-431d-88d0-2add91f4744e/image.png)

<aside>
💸

Most Affordable City by average price in euro 

</aside>

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/4f7a9d21-bebd-418e-8323-7a17bc0ba5fe/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/0da7cf68-c9e3-47fc-812e-b1f158226a49/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/0c113e48-374b-4434-8bb6-c6e76be2b341/image.png)

### Answering the research question according to our findings

*What factors impact and the most significantly Airbnb listings prices in major European cities ?*

<aside>
📢

Most significant across all cities 

</aside>

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/49b14f3c-4350-4e32-8ef8-bb70d1bf603e/7fd535ec-ec86-4481-b132-57ac5e518af8/image.png)

<aside>
📢

Most significants factors in Rome, Barcelona and Lisbon 

</aside>
