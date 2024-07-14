# Airbnb Toronto Listings
**Purpose and Context:** Airbnb currently has more than 5 million hosts and more than 7.7 million active listings. Some of these listings are highly profitable and some are not. In this exploratory project, we are driven in identifying factors that contributes to an Airbnb listing's success. This repository dives into the world of Airbnb listings in Toronto. We perform EDA along with basic supervised and unsupervised machine learning algorithms such as linear regression and K-means clustering.

### Tableau Dashboard and Story
I have added the most important visualizations on Tableau public to make it easy for the stakeholders understand the story of Toronto Airbnb listings. You can checkout my Tableau Storyboard using the following link:
- [Tableau Dahsboard Link](https://public.tableau.com/app/profile/nirav.bariya/viz/AirbnbToronto_17160459621940/AirbnbStory?publish=yes)

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

### Preprocessing the Data
The dataset went through the following series of steps before we the analysis:
1. Explored shape of the data frame, data types of the columns, and summary statistics of the numerical columns.
2. Performed data wrangling by renaming columns and dropping columns.
3. Checked data for consistency addressing mixed data types, handling duplicates, and missing data.
4. Checked data for consistency addressing mixed data types, handling duplicates, and missing data.
5. Calculated summary statistics after consistency check, removed outliers.

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

## Summarizing and Analyzing Data
I started my analysis by performing EDA, identifying distribution of property types and median pricing for each property type.
<p align = "center">
  <img width="80%" alt="image" src="https://github.com/user-attachments/assets/39734b58-58d6-41d5-b1e6-13b5dc3fc213">
</p>

Majority of listings are priced between $50 and $100. As you can see the distribution was skewed right indicating that only few listings were highly priced.
<p align = "center">
  <img width="45%" alt="image" src="https://github.com/user-attachments/assets/25c20310-94bd-401e-9081-8d79b7b46163">
  &nbsp; &nbsp; &nbsp; &nbsp;
  <img width="45%" alt="image" src="https://github.com/user-attachments/assets/dc70bc3f-f6ed-4541-ab17-78ee8e446d92">
</p>

- When it comes to frequency of each property type, we see that entire rental unit, private room in home, entire condo, and entire home are the top 4 types.
- But, the most priced property types do not have high frequency. For instance, Shipping container, entire cottage, boat, Earthen home Entire Villa,  and Island are priced highly but have less frequency. They provide unique value to the tenants.
- The most common type of listings was entire rental unit.

I was interested into visualizing the listings on a map. So, I created a map depicting the number of listings and the median price per neighbourhood.
<p align="center">
<img width="544" alt="image" src="https://github.com/b-N-I-R-A-V/Airbnb_Toronto_Analysis/assets/153047871/23aa1377-7c24-4d7d-bd36-c8f699bf5318">
</p>

Neighborhoods certainly effected pricing of a listing. Following are some of the observations:
- Waterfront Communities Island by far has the most number of listings. The other populated neighbourhoods such as Niagara, Annex, Trinity-Bellwoods, and Church-Yonge corridor are in Downtown Toronto.
- Interestingly, the priciest neighbourhood Forest Hill South, $223, has only 27 listings. This is followed by Bridle Path-Sunnybrook-York Mills, Bay Street Corridor, and Forest Hill North.

It is clear that prices vary in the neighbourhoods. Certain neighbourhoods may influence the pricing of the listing. For instance, a neighbourhood of only Villas. However, whether or not if it is only a consequence of neighbourhood is to be determined.

## Searching for Successful Listings
After performing EDA, I shifted my attention to understanding what makes an Airbnb listing successful. How do I define success? One easy way for me to simplify this definition was to know for how many days a listing goes vacant. That is, how many days in the next 60 or 90 days is it available? I developed a research hypothesis that maybe if a listing is available for many days in the next 60 days, it will be available for many days in the next 90 days.
<p align = "center">
  <img width="80%" alt="image" src="https://github.com/user-attachments/assets/df9d34fe-0b19-4f44-b5cb-964352fb199e">
</p>

- Indeed there was a linear relationship involved. In this case we got an R-squared value of 0.93. This means that the  93% of the variation in availability in the next 90 days can be explained by availability in the next 60 days.
- However, we must be cautiaous while interepreting this results as there is Mean Squared Error(MSE) of 70.78. This means that our predictions could be off by approximately 7 or 8 days. 

I then moved on to perform the K-Means Clustering algorithm to identify successful listings and what contributed to their success. I also examined how the clusters related to price and the number of bedrooms.
<p align = "center">
  <img width="801" alt="image" src="https://github.com/user-attachments/assets/832062f4-289f-4781-b6c4-5d89e66581a6">
</p>
Note that after clustering the data, cluster 0 accommodates more people and has more bedrooms  than any other clusters. Cluster 1 and 2 are priced less than cluster 0 and accommodates fewer people and bedrooms.

<p align = "center">
  <img width="488" alt="image" src="https://github.com/user-attachments/assets/be101faa-1e0f-42de-9e83-70232f37386b">
</p>

Cluster 0 has the highest median price at $300. On the other spectrum cluster 1 has the lowest median price of $65. Cluster 2, 3, and 4, have prices somewhere in the middle. We can think of clusters in terms of price as follows:
- Cluster 0: Very high-priced listings
- Cluster 1: low priced listings
- Cluster 2: medium priced listings
- Cluster 3: medium-low priced listings
- Cluster 4: medium-high priced listings















