# Opening a new pizzeria in Naples? Use Machine Learning to know where!
## 1. Introduction
### 1.1 Background
One of the most popular meal in the world. Someone says that it comes from Turkey, others from Italy. Pizza has radically changed the world, in particular in Naples, the city considered as the birthplace of that disc of dough with tomato souce, mozarella and fresh basil. In the [Wikipedia Pizza page](https://en.wikipedia.org/wiki/Pizza) it can be found a fully description on the history, ingredients and way of cooking. Furthermore, many variants are present, like neapolitan or roman style.  
In this project we want to give an overview of the different borough of Naples, and analyze the optimal place for opening a new pizzeria. We will see that same area of Napoli are full of pizzeria, and so a detailed analysis is needed. Furthermore, we will analyze insight from top pizzeria in Napoli, for example if they have public facebook, instagram page and so on. We all now that nowadays, the success of a venue is partially done to how much it is invested in marketing, and so sponsorizing what you do and your products is the key.

<p align="center">
<img src="https://i0.wp.com/www.napolimilionaria.it/wp-content/uploads/2020/01/ricetta-pizza-sorbillo-impasto-margherita-napoeltana.jpg">
<center>Pizza margherita in its beautiness.</center>
</p>

## 2. Data, resources and methodologies
### 2.1 Data
We will use different sources of data for getting all the information:
- **geographical information**: boroughs will web-scraped from Wikipedia (link [here](https://it.wikipedia.org/wiki/Quartieri_di_Napoli)) and their coordinates using `geopy`;
- **demographical information**: we will web-scraped number of residents per borough from Wikipedia (link [here](https://it.wikipedia.org/wiki/Municipalit%C3%A0_di_Napoli));
- **borough boundaries**: zip file from the official website of Naples townhall will be downloaded, containing the data of borough's boundaries (link [here](http://www.comune.napoli.it/flex/cm/pages/ServeBLOB.php/L/IT/IDPagina/29771));  
- **venues**: we will use Foursquare API (https://developer.foursquare.com/) for obtaining all venues in the city of Naples, and in particular pizzerias. We will use different APIs for getting venues and details (rating, social page, number of tips etc.);

### 2.2 Resources
Many resources will be used in order to web-scrape data, to download from website and to do data manipulation:
- `pandas`: we will use pandas for scraping from wikipedia (since they are in tabular form, there is no needing to use specific web-scraping libraries);
- `numpy`: useful for feature engineering (like one-hot encoding);
- `sklearn`: best library for machine learning. In particular, we will use clustering algorithms in order to clusterize boroughs based on their similarity;
- `folium`: one of the most used library for geoplotting. It allows high flexibility and customization.

### 2.3 Methodologies
For detecting the best place where opening a new pizzeria, we will use k-means algorithm, that is a clustering distance-based method that will help to clusterize similar places.
What we will do next is to analyze the top pizzeria to understand if there are some insight that we can embed.
