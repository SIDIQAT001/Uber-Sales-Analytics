# Uber-Sales-Analytics
This comprehensive dataset contains detailed ride-sharing data from Uber Operations for the year 2024, providing rich insights into booking patterns , vehicle performance, revenue streams , cancellation behaviours , and customer satisfaction metrics.

The goal of this analytics is to uncover insights from the data and make valuable recommendation for the company.

##### Objectives of the analysis
1. DATA IMPORTATION
2. DATA EXPLORATION
3. DATA CLEANING
4. BOOKING PATTERNS
5. CUSTOMER RATINGS
6. DISTRIBUTION OF VEHICLE TYPES


   ## Data and Library Importation
 ```python
# importing the necessary libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import warnings
warnings.filterwarnings('ignore')
```

```python
# importing he dataset
df = pd.read_csv("/content/drive/MyDrive/Colab Notebooks/UBER ANALYTICS/ncr_ride_bookings.csv")
```



# Data Exploration
### Data Snapshot
![](data_head.png).


Before the commencement of the analysis, the data was examined which included process like checking shapes of the data , the data types and missing values.The results of the exploration revealed that the dataset has about 150,000 rows .Certain data fields like , 'Avg VTAT	'(10500 ),Avg CTAT'(48000) ,'Cancelled Rides by Customer'	(139500)  ,'Reason for cancelling by Customer'(139500), 'Cancelled Rides by Driver'(	123000) ,'Driver Cancellation Reason'(123000) ,'Incomplete Rides'(141000), 'Incomplete Rides Reason'(	141000) ,'Booking Value'(48000) ,'Ride Distance'	(48000 )',Driver Ratings'( 57000), 'Customer Rating'	(57000), 'Payment Method'(48000)

## Check for Outliers
![boxplot](boxplot.png).


## Summary Statistics
![summary statistics](summary_statistics.png).








## Data Preprocessing
The data had to be adequately prepared before moving ahead with our analysis therefore, :
* Handling the missing values by removing data :
``` python
# Dropping off data fields with so much missing values
df.drop(["Cancelled Rides by Customer","Reason for cancelling by Customer","Cancelled Rides by Driver","Driver Cancellation Reason","Incomplete Rides","Incomplete Rides Reason"],axis=1,inplace=True)
``` 



# Replacing missing values in our numerical fields with median 
```python
# replacing the missing avg vtat with the median
df['Avg VTAT'].fillna(df['Avg VTAT'].median(),inplace=True)

# replacing the missing avg vtat with the median
df['Avg VTAT'].fillna(df['Avg VTAT'].median(),inplace=True)

# replacing the missing booking value with the median
df['Booking Value'].fillna(df['Booking Value'].median(),inplace=True)


# replacing the missing Customer rating with the median
df['Customer Rating'].fillna(df['Customer Rating'].median(),inplace=True)

# replacing the missing Driver Ratings with the median
df['Driver Ratings'].fillna(df['Driver Ratings'].median(),inplace=True)

# replacing the missing Rides Distance with the median
df['Ride Distance'].fillna(df['Ride Distance'].median(),inplace=True)
```
```python
## Replacing missing values in the rest of the categorical fields with mode
# replacing the missing payment method with the mode
df['Payment Method'] = df['Payment Method'].fillna(df['Payment Method'].mode()[0])
```

## converting the date field into a proper data 
# converting the date column to a proper date data# converting the date column to a proper date set
df['Date'] = pd.to_datetime(df['Date'])

# extracting day from date
df['Day']= df['Date'].dt.day
# extract month from date
df['Month'] = df['Date'].dt.month
# extract year from date
df['Year'] = df['Date'].dt.year
```




## Business Insights
1.What is the pattern of the customer bookings




