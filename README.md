# Ex.No: 01 PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:

### Developed by: G Chethan Kumar
### Reference Number:212222240022

## POPULATION:
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("POPTHM.csv",parse_dates=["DATE"],index_col="DATE")
df.head()
df["2015"].mean()
df.resample('Y').mean()
mean=df.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Population(in Thousands)")
plt.show()
```
## MARKET PRICE
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("trainset.csv",parse_dates=["Date"],index_col="Date")
df.head()
df.Close.resample('M').mean()
mean=df.Close.resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Price")
plt.show()
mean=df.Close.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Price")
plt.show()
```
## TEMPERATURE
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("DailyDelhiClimateTrain.csv",parse_dates=["date"],index_col="date")
df.head()
mean=df["meantemp"].resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Temperature")
plt.show()
```


# OUTPUT:
## Population
![img1](https://github.com/user-attachments/assets/c3eef254-5ce2-423a-ac16-bfad3a478697)

## Stock price
![img2](https://github.com/user-attachments/assets/a5e09bca-fd5d-42ff-b518-0af63856cac0)

![img3](https://github.com/user-attachments/assets/bd9afc72-a0d7-48c7-8e3c-f96e317643b9)
## Temperature

![img4](https://github.com/user-attachments/assets/2325ec8c-9e90-4b32-a466-6e3767d00348)

# RESULT:
Thus we have created the python code for plotting the time series of given data.
