# QA-python-for-DA

## House Data Prediction Model

### Problem statement
Use the kc_house_data.csv dataset to develop an analysis model for estimating house prices in King County, Washington State, USA.

The dataset consists of historic data of houses between May 2014 and May 2015. 
(Source: Kaggle.com). 

This model was put together using Python, in combination with external libraries:
-	NumPy: for working with numerical data
-	Pandas: for manipulating data and data analysis
-	Matplotlib: a plotting library extension of NumPy

### Cleaning the raw data
Raw data was imported into Python as a dataframe using Pandas, containing 21613 rows and 21 columns. 

Our first task was to clean the data, to ensure data that was not useful in developing the problem statement could be eliminated. 

**Removed columns**

Id
Waterfront
View
Condition
Grade*
Yr_renovated
Zipcode
Areas of contention

A big discussion was held around whether zipcode should be included. Is this a relevant data point to predicting house prices? Yes, it is, but the datapoint itself does not help us to create a correlation with price. This is particularly the case if we are looking for a predictive model that would have relatively universal use, rather than just for the King County area. Ultimately, it was felt that longitude and latitude might be better factors to include, as they relate to unchanging data. 

### Areas of uncertainty
We were unsure of what some of the data collected was (condition, grade).


### Columns considered irrelevant
While there was agreement that properties with a waterfront view, or a ‘nice’ view in general would probably sell at a higher price than otherwise similar properties without, when we performed an initial analysis, there 21,434 properties out of 21613 had ‘0’ . This datapoint was felt to be irrelevant as a predictor of house prices in particular case.

### Attempting correlation
Using the seaborn library, we created a heatmap that took a big picture look at house price versus the other factors in our dataset:

- The two strongest correlating factors were number of bedrooms and sqft_living

From this, we were able to see that certain columns seemed to have very little correlation to the house price:
-	Sqft_lot

We then looked at creating a scatter plot to see visually how factors such as number of rooms

### Conclusions
We didn’t have time to complete all the investigations that we would have liked, added to which, as this was this was the first time that we had run this exercise we weren’t always sure of what we were doing.

If I were to complete this exercise again, I would look to spend more time understanding and analysing the data; some of the columns we weren’t sure what they were or if they were important/relevant. Then, probably plot the three or four most correlated columns against price.

Another thing I would like to understand better is how to map the geographical location better to price, either by using zipcode or long/lat. This would surely have a strong correlation with price, but we weren’t able to use this data with relevance.


