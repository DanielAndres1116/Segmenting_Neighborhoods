# Segmenting Neighborhoods by features of venues inside it

This link is to see better the Notebook: https://nbviewer.jupyter.org/github/DanielAndres1116/Segmenting_Neighborhoods/blob/main/Clustering-Venues.ipynb
The previous link for see the maps that we could not see on the principal file ipynb.

## Dataset

The dataset was obtained from a Wikipedia Web Page where there is a list of postal codes in Canada located within the city of Toronto. This is the link: https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M. This data was retrieved thanks Webscrapping techniques by using Beautifulsoup library. Also was downloaded a CSV file which has inside the data of latitude and longitude for each Postal Code, but it would be possible obtain this data using Geocoder, but at moment of do the program it doesn't work, but this is fixable.

The next image is a part of the table in wikipedia web page where we extract the data:

![image](https://user-images.githubusercontent.com/43154438/119295146-b4e55780-bc1b-11eb-9dd5-bfc3d7b95d56.png)

Also was used the FourSquared API to extract information about popular venues inside the neighborhood, for example, data of restaurants, airports, hotels, food trucks, parks, cinema, etc. All this thanks Developer Account in FourSquare API and the JSON files that allows us to see. 

The next is a little look at what we could extract from the Foursquare app. Among what users are, places, location scores, kind of things that are sold and opinions from other people.

![image](https://user-images.githubusercontent.com/43154438/119295365-43f26f80-bc1c-11eb-9e69-578a131c5033.png)

## Objectives

Create an Unsupervised Machine Learning Algorithm (more specifically K-Means) to do a segmentation of the neighborhoods in Toronto for analyze similar characteristics due the kind of venues inside them, and this is possible by analyzing the mean of frequency of ocurrence of each category. This could be of great help for people who want locate certain venue as stall, food truck, park, airport, hotel, coffee shop, clothes shop, etc. And not only for that, because this could give us a great idea of the disposition of places to plan many types of strategies, as a travel map, where to go to get certain service or product, and even for demographic analysis. 

## Tools and libraries used

![image](https://user-images.githubusercontent.com/43154438/119296000-c2034600-bc1d-11eb-98e4-d3489086501d.png)

The library of pandas was used for all program to do the processing of data. 

The BeatifulSoup library was used to do webscrapping from the wikipedia web page. 

Folium was the library used to put the places points on the map according to the latitude and longitude coordinates retrieved previously of the locations on Toronto. 

In conjuntion with the previous library, was used matplotlib library to make the presentation of the map more pleasant by giving colors to the dots and distinguish between clusters.

It was used the library to handle JSON files and manage the data obtained from Foursquare API about the popular venues. 

Finally, the library of sklearn was used to do KMeans as our model of clustering.  

## Results And Conclusions





