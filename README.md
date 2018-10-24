# FindYourNeighborhood
## Introduction  
This project is designed to help people find the similar neighborhood in Houston as the one they are fond of. It can be useful for business expansion like choosing a new branch’s location, or for the new comer to choose the comfortable place to settle down with the similar environment as the one they’ve enjoyed before. 

So basically, this project would ask user for two inputs. One is the zip code for the template neighborhood. The other one is the target zip code for the possible neighborhoods. Then the project would analyze the data of the surrounding venues for the template zip code by Foursquare (in a small radius), and compare the similarity with the neighborhoods from the target zip code (in a larger radius). The result would demonstrate the top three neighborhoods with the highest similarities for user to choose. 
## Data  
**The data required to accomplish this project will include::**  
1.  List of postal codes with their corresponding coordinates in the US. https://gist.github.com/erichurst/7882666  
    A pandas dataframe displaying postal code, latitude, longitude can be generated from the .csv file by these data.

2.	List of postal codes with their corresponding neighborhoods in Houston.  https://www.houstoniamag.com/articles/2017/3/24/neighborhoods-by-the-numbers-real-estate-data-2017  
    The data need to be scraped from web page by BeautifulSoup first for use. Then combine it with the dataframe from data 1 to make a new dataframe showing the postal code, neighborhoods and coordinates in Houston.

3.	Data of venues in the surrounding area of the particular coordinates from Foursquare.  
    Make the API request to Foursquare for the data of the venues at the queried coordinates which come from the dataframe made by data 1 and data 2. Segment the neighborhoods by their venues categories to find out the top three neighborhoods with the highest similarity to the template.
