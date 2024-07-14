# Airbnb Toronto Listings
**Purpose and Context:** Airbnb currently has more than 5 million hosts and more than 7.7 million active listings. Some of these listings are highly profitable and some are not. In this exploratory project, we are driven in identifying factors that contributes to an Airbnb listing's success. This repository dives into the world of Airbnb listings in Toronto. We perform EDA along with basic supervised and unsupervised machine learning algorithms such as linear regression and K-means clustering.

### Project Goals:
- Identify successful listings
- Determine factors that makes a listings successful
- Determine pricing pattern

## Tools and Techniques
For this project I have used Python including libraries such as Numpy, Pandas, Sci-kit learn, Matplotlib, Seaborn, and Folium for maps. To share the outcomes I have used Tableau Public.
Additionally, the following is a brief list of techniques that were used in this project:
- Data wrangling
- Data Cleaning and summarizing
- Correlation Analysis
- Linear Regression
- K-Means Clustering

## Dataset
The dataset I have used is an external dataset. The data was collected by insideairbnb.com and not published by Airbnb itself. The website however is not endorsing nor associated with Airbnb or its’ competition. The website claims that the data compiled is for public analysis, discussion, and community website. In my opinion, I think we can consider this data set as trustworthy since it is collected from Airbnb and due transparency is shown by Inside Airbnb. 
- [Inside Airbnb Data Source](https://insideairbnb.com/get-the-data)
- [Toronto Listings Data set](https://data.insideairbnb.com/canada/on/toronto/2024-05-09/data/listings.csv.gz)
- [GeoJSON file of Neighbourhoods in Toronto](https://data.insideairbnb.com/canada/on/toronto/2024-05-09/visualisations/neighbourhoods.geojson)

### Challenges

- I noticed that 25% of the price were missing in the original data set. This was challenging as I wanted to predict price of an Airbnb listing and imputing the price using any technique would have defeated the purpose of doing so.
- To handle these missing values, I had to remove them from the dataset. This may have skewed the data in one direction or another and may case bias in the data. Therefore, results of this analysis can be interpreted with caution.
- The primary goal of the project was to practice skills with machine learning algorithms.


## Key Questions
1. Which neighbourhoods are most populous, and which neighbourhoods have higher pricing?
2. What is the relationship between the number of bedrooms offered and the pricing of a listing?
3. What is the distribution of property types and room types in Toronto?
4. Is there any relationship between property type and price? Which property types are costly?
5. Do customers prefer fewer minimum nights or more minimum nights?
6. Which factors are related to listings that are most successful?

<div align="center">
<img width="544" alt="image" src="https://github.com/b-N-I-R-A-V/Airbnb_Toronto_Analysis/assets/153047871/23aa1377-7c24-4d7d-bd36-c8f699bf5318">
</div>

## Data Limitations and Challenges
I noticed that 25% of the price were missing in the original data set. This was challenging as I wanted to predict price of an Airbnb listing and imputing the price using any technique would have defeated the purpose of doing so. To handle these missing values I had to remove theem from the dataset. This may have skewed the data in one direction or another and may case bias in the data. Therefore, results of this analysis can be interpreted with caution. The primary goal of the project was to practice skills with machine learning algorithms.


## Tableau Dashboard and Story
I have added the most important visualizations on Tableau public to make it easy for the stakeholders understand the story of Toronto Airbnb listings. Note that, not all the visualizations have been added to the Tableau dashboard.

[Tableau Dahsboard Link](https://public.tableau.com/app/profile/nirav.bariya/viz/AirbnbToronto_17160459621940/AirbnbStory?publish=yes)




