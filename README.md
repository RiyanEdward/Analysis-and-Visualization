# Analysis-and-Visualization
Analysis and Visualization Melbourne Housing Dataset

**Context**

A real estate company has sales data from 2016-2018, the company wants to have knowledge about the distribution of houses by type and location. So when a customer comes to buy a house with a certain desire, the real estate agent can find out which house is suitable for that customer


**Goals**

The company wants to have the ability to provide recommendations for suitable homes for each of its customers, so that it can increase sales through the company

**Analytic Approach**

So we do statistical tests with the help of visualization so that the process of analysis is easier to interpret

**Data Understanding**

This is a dataset created by Tony Pino.

It is drawn from publicly available results posted weekly from Domain.com.au. He cleaned it up nicely, and now it's up to you to work the data analysis magic. The dataset includes Address, Property Type, Suburbs, Method of Sale, Room, Price, Real Estate Agent, Date of Sale and Distance from C.B.D.

https://www.kaggle.com/datasets/dansbecker/melbourne-housing-snapshot

# Data Cleaning

Dropped columns:
* Bedroom 2: the contents of this data are the same as in the Rooms column, so we only use one of them
* YearBuilt: dropped because it has quite a lot of missing values ​​and cannot be filled in based on domain knowledge
* Propertycount : there is no explanation about this column on kaggle, it is better to drop it because it is not used for analysis too
* Address: because this analysis is not about the customer profile, so we drop it because it is not used for this analysis

Handling missing values ​​:
* Missing value in the column is filled using the median of the column
* councilArea is filled with 'NC' to indicate that the row is missing value
* Building Area is filled using KNN Imputer

# Summary

From the overall analysis, it can be concluded that the thing that greatly affects house prices is the region. This certainly makes sense because the metropolitan region is near the CBD (central business district), the facilities available near the CBD are definitely better than facilities in areas far from the CBD. The type of house also greatly affects the selling price while the time, area of ​​land and buildings, and the number of rooms if based on the results of the correlation have a moderate or not too large effect.

Can be **recommended** for potential home buyers in the city of melbourne:

* If you want to buy a house near the CBD, you can buy it at Northern Metropolitan. In this region, the availability of houses, townhouses and duplexes is quite a lot, the prices are also lower than Western and Southern Metropolitan. Maybe because the average building area is smaller than the average building area in western and southern metropolitan areas.

* If you want to buy the cheapest house, you can buy a house in western victoria. you can buy a house with a large enough land area at a fairly affordable price, cheaper than unit prices in the entire metropolitan region. But to buy a house here means you buy a house that is quite far from the CBD

* If you want to buy the most expensive house, you can buy a house in the Southern Metropolitan area. even the price of 1 duplex here is equivalent to buying 3 houses in western victoria. It should be further analyzed beyond this data why homes in the southern metropolitan are so expensive.

* If you want to buy a house that is far from the crowds or far from the CBD, you can buy a house in Eastern Victoria. by spending the same amount of money as buying a Townhouse house in the Northern Metropolitan(nearest to the CBD), you can buy a house with a land area of ​​up to 3000
