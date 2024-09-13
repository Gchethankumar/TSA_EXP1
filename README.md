#### Developed by:  G Chethan Kumar
#### Reference No:  212222240022
####  Date: 

# Ex.No: 01 PLOT A TIME SERIES DATA

# AIM:
To Develop a python program to Plot a time series data of a Company's Revenue.

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.

# PROGRAM:
```
import pandas as pd
import matplotlib.pyplot as plt

data= pd.read_csv('india-gdp.csv',nrows=50)
print(data.head())
data['date'] = pd.to_datetime(data['date'], format='%d-%m-%Y')
data.set_index('date',inplace=True)
```
```
plt.plot(data.index,data['AnnualChange'],label='AnnualChange')
plt.title("India's Annual % change in GDP")
plt.xlabel("Year")
plt.xticks(rotation=45)
plt.ylabel("Annual % Change")
plt.grid(True)
plt.legend()
plt.show()
```

# OUTPUT:

![Screenshot 2024-09-13 085933](https://github.com/user-attachments/assets/51faee9b-2559-4eec-8a96-3e31b3445d46)

# RESULT:
Thus we have created the python code for plotting the time series of given data.
