# Restaurant_Recommendation

The objective of this project is to develop a restaurant recommendation system designed to provide customers with personalized suggestions for 1-3 restaurants, tailored to their specified filters and preferences.

Filters which the customers will be using are on **Location**, **Cuisine** and **Rating**. 

## Data Collection:
Primarily data has been collected from "FoodPanda" website along with Google Maps for Map Link addition. Firstly, we collected _restaurant names, cuisine and rating_ from FoodPanda however extracting map links proved challenging. Thus, attempts were made to scrape data from various websites but each had its limitations so we decided to move forward with the data from earlier source and using the area/location name from that csv file,we added [map link](scraping_map-generation.ipynb) by  sending the location of restaurants to Google Map and using the map's share option, the resulting map links were copied and incorporated into the dataframe.

The subsequent phase of the project involves model building and deployement, which is currently underway.


_Please note that as this project is intended for industrial use, the exact code and data can not be disclosed. Nonetheless, a partial view of the data, featuring only four locations, is accessible [here](dmd-gulshan-banani-wari.csv). It's worth noting that the dataset encompasses restaurants from over 30 locations._

## Challenges
1. The precise details, such as the road number and house number, for the restaurants could not be retrieved from FoodPanda. Later on, the necessity for exact locations was disregarded, given that contemporary individuals  rely on Google Maps. Nonetheless, even in this scenario, the maps were unattainable. 
2. Then attempts were made to scrap restaurant data from Google. Unfortunately, the data lacked cuisine details, and ratings were also absent, despite having the desired maps.
3. Following this, a decision was made to combine data from both sources to obtain the desired columns. However, in doing so, it was discovered that there were a maximum of 30 common restaurants from each location. Proceeding with such limited data would have resulted in a significantly small dataset.
4. Finally, the FoodPanda dataset was utilized, and an automated search was conducted for each restaurant's location in Google Maps through selenium. This process yielded the distinctive map links that were sought.
