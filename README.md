# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
In this project I will be requesting data from the City Bikes, FourSquare and Yelp API's
and then reading that data from JSON format into pandas dataframes. After that I will be
looking at the correlations between the number of free bikes in the city of Vancouver, BC
compared to the statistics of various points of interest in the same city.

##Instructions
### First run city_bikes.ipynb. It will grab the data from the City Bikes API using an http request and store the data as a dataframe and csv file.
### Next run yelp_foursquare_EDA.ipynb. This does the same thing as the first file but does it for the FourSquare and Yelp API's.
### After that run joining_data.ipynb. This file joins the data from the City Bikes and FourSquare API's and then shows plots comparing data and a correlation heatmap
### It also takes the joined data and creates and sql table and stores that.
### Finally run model_building.ipynb. This will use the data from joining_data.ipynb to perform linear regression and other correlation statistics on the data.

## Process
### First I use and http request to grab data from each of the API's listed above.
### I parse through the data to see what city has data from each of the API's and how the data is structured.
### Then I take the data that I get and turn it into pandas dataframes for easier access and comparison.
### Then I use linear regression and correlation statistics to compare the data to find relationships between the data from the various API's.

## Results
The FourSquare API allowed me to gather information as they had more fields I could query from their website
while for Yelp I could not find any documentation on the fields I could get so the default request had less information.
After looking at the correlation from variables gathered from the FourSquare API against the amount of free bikes in the City Bikes API, 
I did not find any correlations with a value >0.2 which means there was a lack of correlation between variables individually. 
Then using multivariate linear regression I compared the amount of free bikes to all the variables collected and it came out with
an R-squared of only 0.113 which means that the independent variables are not explaing the variance of the free bikes.

## Challenges 
The biggest challenge is the use of a new API and getting familiar with how to call from it and how the data is stored.
For example the FourSquare API did not show all the data it actually holds on a simple get request so I had to look
through its documentation to find fields I wanted. On the other hand for Yelp I could not find any such documentation
and since I was calling it too often I eventually ran out of requests and was unable to use the API for the rest of the project.

## Future Goals
1. I would like to spend more time looking through the Yelp API to try to find more data to add to the models in the project.
The hope would be to combine the Yelp and FourSquare API's to get a better picture.

2. Since I could not find any correlations between the variables I gathered I would like to take a deeper look at what other
variables I could find that may indicate the usage of bikes in Vancouver.
