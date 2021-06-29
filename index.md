![cover_image](https://user-images.githubusercontent.com/26163704/123705104-63556b80-d85e-11eb-9ce1-2a2c99f593b3.jpg)

# THIS is what affects Ireland's Airbnb prices
#### An Analysis of Ireland's Airbnb Listings Data and How YOU Can Use It To Your Advantage
---
##### Author: Sorcha Nic Conmara | June 2021
---

In this article, I will dicuss my findings from analysing Airbnb data on listings in Ireland. The [data from Ireland](http://insideairbnb.com/get-the-data.html) is free to access and was scraped from the Airbnb website in March, 2021. The data dictionary can be accessed [here](https://docs.google.com/spreadsheets/d/1iWCNJcSutYqpULSQHlNyGInUvHg2BoUGoNRIGa6Szc4/edit#gid=982310896).

#### What is Airbnb?
> Airbnb is an online marketplace that connects people who want to rent out their homes with people who are looking for accommodations in that locale. It currently covers more than 100,000 cities and 220 countries worldwide and has millions of hosts and travellers using it.

In Ireland, as of March 2021, there were over **26,000 listings**
and that number is growing as more and more people realise what a **great opportunity it is to make some extra cash**. In this blog post, I will reveal some of the key insights I discovered from analysing the Airbnb listings data for Ireland.


My first question was a simple one:
> 1. **Where in Ireland are Airbnbs the most expensive?** 

To my surpise, the most expensive listings based on average listing price were in County Louth. Leitrim, for example, is the county with the smallest population in the country yet it had the 4th most expensive average listing price. 
<img src="https://user-images.githubusercontent.com/26163704/123715043-69a01380-d86f-11eb-86aa-aa12f3cda10d.png">

This seemed odd, and upon investigating the distribution of AirBnBs, we can see that they are not equally distributed across Ireland and also the price distribution is skewed. Therefore, the average price isn't a fair representation to group by. Any county with fewer listings (such as Louth), only needed one very expensive listing to pull its mean listing price up, which is likely what happened. 

<img src ="https://user-images.githubusercontent.com/26163704/123715070-77ee2f80-d86f-11eb-92a8-bc8da946be13.png" align="right" width = 45%> 
<table class="tg">
<thead>
  <tr>
    <th class="tg-dvpl">region_parent_name</th>
    <th class="tg-0pky">number of listings</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-dvpl">Dublin   City Council</td>
    <td class="tg-dvpl">5889</td>
  </tr>
  <tr>
    <td class="tg-dvpl">Kerry   County Council</td>
    <td class="tg-dvpl">2841</td>
  </tr>
  <tr>
    <td class="tg-dvpl">Donegal   County Council</td>
    <td class="tg-dvpl">1971</td>
  </tr>
  <tr>
    <td class="tg-dvpl">Cork   County Council</td>
    <td class="tg-dvpl">1801</td>
  </tr>
  <tr>
    <td class="tg-dvpl">...</td>
    <td class="tg-dvpl">...</td>
  </tr>
  <tr>
    <td class="tg-dvpl">Laois   County Council</td>
    <td class="tg-dvpl">163</td>
  </tr>
  <tr>
    <td class="tg-dvpl">Offaly   County Council</td>
    <td class="tg-dvpl">139</td>
  </tr>
  <tr>
    <td class="tg-dvpl">Monaghan   County Council</td>
    <td class="tg-dvpl">132</td>
  </tr>
  <tr>
    <td class="tg-dvpl">Longford   County Council</td>
    <td class="tg-dvpl">60</td>
  </tr>
</tbody>
</table> <br/>


When comparing this with the listing price grouped by the median (the middle price, when price is ordered), we can see a slightly more realistic overview of Airbnb prices in Ireland. However, to my surprise, Louth has the 2nd most expensive median Airbnb listing prices. Also very surprising is that South Dublin was the cheapest when listing prices were grouped by median.

<img align="left" src="https://user-images.githubusercontent.com/26163704/123714511-5b052c80-d86e-11eb-8637-e94b08445979.png" width="45%"> <br/>

My second question was related to the growth of Airbnb:
> 2. **What counties have the fewest AirBnBs and could be areas potential hosts may consider listing a property in? Also, what kind of rooms are most popular in Ireland? (and therefore be considered by potential hosts)**

If you're considering becoming an Airbnb host, you might want to consider hosting in Longford, Monaghan or Offaly. These are the three regions with the fewest Airbnbs in Ireland and are therefore an investment opportunity, especially considering how popular Airbnbs are becoming.

If you are thinking about becoming a host, it is worth knowing what the most common property types are to see if what you can offer is unique.

![property_type](https://user-images.githubusercontent.com/26163704/123715073-7c1a4d00-d86f-11eb-8836-9996b97067f7.png)

My third question was all about the **what** 
> 3. **What features affect the listing price? And to what extent? i.e. what can YOU do to your Airbnb to increase its value?** 

I was surprised to learn that for Ireland, a superhost status doesn't make much of an impact on price listing. 

> Superhosts are experienced hosts who provide a shining example for other hosts, and extraordinary experiences for their guests.

I assumed that people would likely expect to pay more to stay in a superhost's listing but this doesn't seem to be the case as both distributions are very similar. A superhost status seems to pissbly have a slight impact on the `Review Scores Rating`, but only just.

<img src="https://user-images.githubusercontent.com/26163704/123717052-f0ef8600-d873-11eb-8614-9f37ea7951a6.png" width=45%>
<img src="https://user-images.githubusercontent.com/26163704/123717060-f351e000-d873-11eb-8474-5b1b793596e2.png" width=45%>

![bed_bath_vs_price](https://user-images.githubusercontent.com/26163704/123717532-f5686e80-d874-11eb-9a94-6fc542bb0819.png)
 - does the number of bedrooms/bathrooms affect price? 
 - ![bedrooms_vs_median_price](https://user-images.githubusercontent.com/26163704/123717562-031df400-d875-11eb-94ed-5ee2fb6e8b39.png)


 - does the number of reviews/overall review score rating affect price?
 ![reviews_vs_price](https://user-images.githubusercontent.com/26163704/123717595-116c1000-d875-11eb-90c6-73524af646b8.png)
   
My final question was as follows:

> 4. **Can the price of a listing be predicted? What are the most influential features in predicting price?**

 ![lr](https://user-images.githubusercontent.com/26163704/123717625-1f219580-d875-11eb-884f-e07240ac5114.png)

![hostver_impact](https://user-images.githubusercontent.com/26163704/123717675-39f40a00-d875-11eb-879f-653ed3164b66.png)
![region_impact](https://user-images.githubusercontent.com/26163704/123717677-3bbdcd80-d875-11eb-83f0-0a3b7f76ca7e.png)
