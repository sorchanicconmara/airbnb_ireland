**airbnb_ireland**

# Brief Analysis of listings data for AirBnB in Ireland from March 2021. 
#### Includes some exploratory data analysis (EDA), visualisations and modelling to attempt to answer the following:
---

#### Author: Sorcha Nic Conmara | June 2021

### The motivation for the project was to answer the following questions:

1. **Where in Ireland is the mean/median price for an AirBnB the most expensive?** Is it in Dublin where house prices tend to be the most expensive? The median price may be a better measure here as outliers in price from counties with fewer AirBnBs may skew the data.


2. **What counties have the fewest AirBnBs and could be areas potential hosts may consider listing a property in?Also, what kind of rooms are most popular? (and therefore be considered by potential hosts)**


3. **What features affect the price of the listing? And to what extent?** 
E.g.:

 - does being a superhost/the hosts review rating score affect price?
 - does the number of bedrooms/bathrooms affect price? 
 - does the number of reviews/days since last review/average overall review score affect price?
    
    
4. **Can the price of a listing be predicted? This could be used by hosts when listing to determine what to charge for the listing.**

### Libraries used:
- seaborn==0.11.0
- scikit-learn==0.23.2
- pandas==1.2.4
- numpy==1.19.1
- matplotlib==3.3.1


This project was created as part of the Udacity Data Scientist Nanodegree program.

### File Structure:

- **Project1_airbnb_data_ireland.ipynb** - Jupyter Notebook containing EDA, data cleaning, visualisations and linear regression model.

- **raw_data/**
    listings.csv.gz -  raw AirBnB data for Ireland from March 2021.
    listings.csv -  unzipped raw AirBnB data for Ireland from March 2021.

### Summary of Results:

1. **Where in Ireland is the mean/median price for an AirBnB the most expensive?** 

The top 3 most expensive regions based on median listing price are:

    1 - Kerry County Council
    
    2 - Louth County Council
    
    3 - Galway City Council


2. **What counties have the fewest AirBnBs and could be areas potential hosts may consider listing a property in? Also, what kind of rooms are most popular? (and therefore be considered by potential hosts)**

The 3 regions which the fewest AirBnB listings are:

    1 - Longford County Council
    
    2 - Monaghan County Council
    
    3 - Offaly County Council
   
The top 2 most popular types of rooms across AirBnB in Ireland are entire home/apt and private rooms.


3. **What features affect the price of the listing?** E.g.:

    - does being a superhost/the hosts' reviews affect price?

Being a superhost does not seem to affect price while the hosts review rating seems to be higher when the host is a superhost.
    
   - does the number of bedrooms/bathrooms affect price?
   
The number of bedrooms and bathrooms usually affects the price, however the increase steadies as the number of bedrooms becomes much larger - e.g. 2 bedroom listings vs 14 bedroom listings.
    
   - does the number of reviews/overall review score rating affect price?

We can see that all hosts who received 7+ ratings in the last 30 days have a review rating score of at least 95%. In terms of price, there still seems to be a relatively wide range for those with 7+ ratings and 95%+ review score rating. This suggests that a combination of these features affect the overall price of the listing. Superhosts also tend to have higher overall Review Score Ratings.
    
    
4. **Can the price of a listing be predicted? This could be used by hosts when listing to determine what to charge for the listing.**

We've seen from the simple Linear Regression model that the region and the host's verification have the strongest impact on predicting the price of a listing.

___
