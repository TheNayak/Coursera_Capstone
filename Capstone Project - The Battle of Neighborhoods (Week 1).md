# IBM DATA SCIENCE: Capstone Project - The Battle of Neighborhoods (Week 1)
Rahul Nayak

## Bringing a new pizza chain into the market in Bengaluru city, India. 

### Some Context:
Vasudev Krishna a hotelier runs a chain of Pizza restaurants under the brand name of Vaikunta Pizzaria in the city of Mumbai, India. Building on the success of his venture he wants to expand his business into a new city of Bengaluru, India. While doing his research Vasudev finds out that his friend Gandivdhari Arjuna, an aspiring data scientist has recently completed the IBM DATA SCIENCE professional certificate. Vasudev has requested Arjuna to help him with his problem.

### Business Problem:
Vasudev wants to expand his Pizza chain into the markets of Bengaluru, India. But first, he must do some research. His main dilemma is to decide as to where will he locate his restaurants in Bengaluru. He wants to expand into areas that have the least pizza restaurants in their vicinity, neighborhoods that are not known for their pizza restaurants. He is confident that his pizza will find buyers as they are literally the food of the gods. Hence he enlists the help of his dear friend Arjuna, who with his recent working with machine learning techniques and the foursquare API has promised Vasudev that he will solve his dilemma. Arjuna has promised Vasudev that he will look up details on all the neighborhoods in Bengaluru and find out which of them have popular pizza places within them and will also compare the commercial real estate prices to get Vasudev the best location with lowest prices for him to set up his restaurant chain.

### Data

Firstmost, a list of neighborhoods in Bengaluru will be needed. This list will be obtained from [here](https://www.mapsofindia.com/pincode/india/karnataka/bangalore/), a table containing neighborhood names with respect to its postal code. This table will have to be read into a dataframe.

Next we will need the latitude and longitude for each neighborhood. for this we will use the geocoding webservice geopy (The documentation can be found [here](https://geopy.readthedocs.io/en/stable/))

Next we will need some commercial real estate prices. Some prices can be found in [this report](http://www.realisticrealtors.in/assets/CIRIL%20Half%20Yearly%20Report.pdf) in pages 19-22.

Next we will use the Foursquare API to make calls (The tutorial can be found [here](https://www.coursera.org/learn/applied-data-science-capstone/home/week/2)) to get the top 10 venues in each neighborhood.  

Next we will use classification technique of K-Means clustering to group the neighborhood into 5 clusters and we will study the top 10 venues in each cluster.

We will suggest Vasudev to open his pizza restaurants in the clusters that don't have pizza restaurants as their top 3 to 5 venues also considering the property prices.
