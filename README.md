# 1. Segmenting neighborhoods according to venues: Is this site a good place to start your business?

## 1.1. An explanation of the Foursquare API used in this project

Foursquare API is a location data platform that provides developers with access to a vast array of location-based data, including data on venues, users, photos, and check-ins. The API is designed to help businesses and developers build location-based applications that provide insights and recommendations to users.

Features of the Foursquare API include:

1.	Venue search: The API provides access to the Foursquare database of over 100 million venues, making it possible to search for specific venues or venues that match certain criteria, such as type of venue, location, and rating.
2.	User information: The API provides access to user data, including user profiles, check-ins, and photos. This information can be used to create personalized recommendations and experiences for users.
3.	Check-in data: The API provides access to check-in data, including the time and location of each check-in, as well as information about the venue where the check-in took place. This information can be used to track foot traffic and understand patterns of behavior.
4.	Photos: The API provides access to photos of venues and users, which can be used to enhance the visual experience of location-based applications.
5.	Tips: The API provides access to tips and recommendations for venues, which can be used to help users discover new places and experiences.

The Foursquare API can be used for people analyzing venues and where their physical business could be placed in several ways:

1.	Location analysis: The API can be used to gather data on foot traffic patterns, demographic information, and the popularity of different venues. This information can be used to make informed decisions about where to locate a business, such as choosing a location with high foot traffic or targeting a specific demographic.
2.	Competitor analysis: The API can be used to gather data on competitor businesses and their locations, helping businesses to understand the competitive landscape and identify potential opportunities.
3.	Personalized recommendations: The API can be used to provide personalized recommendations to users based on their location, check-in history, and other data. This can help businesses to attract and retain customers by providing relevant, targeted recommendations.
4.	Marketing: The API can be used to target specific demographics and locations with advertising, helping businesses to reach their desired audience and drive foot traffic to their location.

Overall, the Foursquare API provides a wealth of location-based data and features that can be used to inform business decisions, personalize user experiences, and drive growth and success.

## 1.2. An explanation of the Web Scraping techniques used in this project

Beautiful Soup is a Python library used for web scraping purposes to extract data from HTML and XML files. It is designed to help developers pull out the required information from websites and work with it in a more structured manner.

With Beautiful Soup, you can parse HTML and XML files, perform searches and find specific elements, extract the required data, and clean and transform it into a format that is suitable for further analysis.

Here are some of the web scraping techniques that can be used with Beautiful Soup:

1.	Parsing HTML and XML files: Beautiful Soup can parse HTML and XML files, and allows you to search for specific elements, such as tags and attributes, within the file.
2.	Searching for specific elements: With Beautiful Soup, you can search for specific elements, such as tags and attributes, within the HTML or XML file, making it easy to extract the data you need.
3.	Extracting data: Once you have found the specific elements you are looking for, you can extract the data contained within them, such as the text or the values of attributes.
4.	Cleaning and transforming data: Beautiful Soup also provides functionality for cleaning and transforming the extracted data, such as converting it to a more structured format, like a pandas DataFrame, or removing unwanted elements, such as HTML tags.
5.	Navigating the DOM tree: Beautiful Soup makes it easy to navigate the DOM (Document Object Model) tree, which is a representation of the structure of an HTML or XML document. This allows you to easily traverse the tree and find specific elements.

Overall, Beautiful Soup is a powerful library that makes web scraping easier and more convenient, allowing you to extract data from websites in a structured and efficient manner.

## 1.3. An explanation of K-Means, the Unsupervised Machine Learning Model implemented

K-Means is an unsupervised machine learning algorithm used for clustering. The goal of K-Means is to group similar data points together into “k” number of clusters, where k is a pre-defined constant. The algorithm works by assigning each data point to the nearest cluster center and then re-calculating the cluster center based on the average of the assigned data points. This process is repeated until the cluster centers converge and no further changes occur. K-Means is commonly used in market segmentation, image compression, and anomaly detection.

## 1.4. Dataset Description

The dataset was obtained from a Wikipedia Web Page where there is a list of postal codes in Canada located within the city of Toronto. This is the link: 

https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M

This data was retrieved thanks Webscrapping techniques by using Beautifulsoup library. Also was used the FourSquared API to extract information about popular venues inside the neighborhood, for example, data of restaurants, airports, hotels, food trucks, parks, cinema, etc. All this thanks Developer Account in FourSquare API and the JSON files that allows us to see.

## 1.5. Objectives of this project

Create an Unsupervised Machine Learning Algorithm (more specifically K-Means) to do a segmentation of the neighborhoods in Toronto to analyze similar characteristics due the kind of venues inside them, and this is possible by analyzing the mean of frequency of ocurrence of each category. This could be of great help for people who want to locate certain venue as stall, food truck, park, airport, hotel, coffee shop, clothes shop, etc. And not only for that, because this could give us a great idea of the disposition of places to plan many types of strategies, as a travel map, where to go to get certain service or product, where should we place our physical business and even for demographic analysis.

## 1.6. Programming Code Explanation

The code is written in python and uses several libraries such as BeautifulSoup, requests, pandas, numpy, ibm_boto3, and geopy.

1.	The requests library is used to scrape the contents of a website (in this case, a wikipedia page) and the BeautifulSoup library is used to extract and parse the table contents of the wikipedia page into a usable format.
2.	The data is then stored in a list of dictionaries and transformed into a Pandas dataframe (df) for easier manipulation. Some data cleaning is performed on the “Borough” column.
3.	The code then accesses a file in IBM Cloud Object Storage, which contains another dataframe (df_data_1) with latitudes and longitudes of different postal codes. The code uses a for loop to match the postal codes in both dataframes and update the latitude and longitude values in the original dataframe (df).
4.	The geopy library is then used to retrieve the latitude and longitude values of Toronto.
5.	Finally, the folium library is used to visualize the data on a map of Toronto, where each neighborhood is marked with its latitude and longitude.

## 1.7. Conclusions and Result Analysis

This is a small sample of the most important venues around the analyzed place. This allow us to make an analyzis of what kind of venues are in certain neighbors:

![image](https://user-images.githubusercontent.com/43154438/229926478-6780a3ce-0975-4160-8949-41c4325e347d.png)

Figure 1: a sample of the most important venues around the analyzed place

I am going to do an analysis of more recurrent venues on the calculated clusters.

•	Cluster 0 is the one that contained the most elements, here are involved the places with many cafes and restaurants. If you want places to eat or drink coffee, these are the sectors.
•	Cluster 1 features music sites, children’s gardens, wings joint and escape rooms. These seems to be places to have a good time and entertain yourself with friends.
•	Cluster 2 has PUB’s, Health food stores, trails, Discount Stores and Distribution Centers. If you want to do good-priced shopping as well as enjoy a good national beer, these are the sectors you should visit.
•	Cluster 3 has Tennis Court, restaurants and trails. If you would like go and spend time doing exercise, these could be sectors to take advantage
•	Cluster 4 has Bus Lines, parks and playgrounds. If you have children in your family, these are places where you could take them.
•	Cluster 5 has convenience stores, event space, Diner and Parks too.

This is a map where I show the assigned clusters.

![image](https://user-images.githubusercontent.com/43154438/229926619-e0b94f60-3502-462e-8a2f-1ea260f7758c.png)

Figure 2: map of the assigned clusters to each neighborhood

There are several things that I would like to improve in this project. Those things are indicated in the last section of this program in my Github repository that you can check in the previous provided link.
