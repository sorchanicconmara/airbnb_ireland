**airbnb_ireland**

Brief Analysis of listings data for AirBnB in Ireland from March 2021. Includes some exploratory data analysis (EDA), visualisations and modelling to attempt to answer the following:

1. **Where in Ireland is the mean/median price for an AirBnB the most expensive?** Is it in Dublin where house prices tend to be the most expensive? The median price may be a better measure here as outliers in price from counties with fewer AirBnBs may skew the data.


2. **What counties have the fewest AirBnBs and could be areas potential hosts may consider listing a property in?Also, what kind of rooms are most popular? (and therefore be considered by potential hosts)**


3. **What features affect the price of the listing? And to what extent?** 
E.g.:

 - does being a superhost/the hosts tenure affect price?
 - does the number of bedrooms/bathrooms affect price? 
 - does the number of reviews/days since last review/average overall review score affect price?
    
    
4. **Can the price of a listing be predicted? This could be used by hosts when listing to determine what to charge for the listing.**

Libraries used:
- include requirements.txt

This project was created as part of the Udacity Data Scientist Nanodegree program.

**File Structure**:

- Project1_airbnb_data_ireland.ipynb - Jupyter Notebook containing EDA, data cleaning, visualisations and linear regression model.
- raw_data/
    listings.csv.gz -  raw AirBnB data for Ireland from March 2021.
