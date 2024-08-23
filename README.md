### Developed by: G Chethan Kumar
### Reference Number:212222240022
###  Date: 

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
```
```
data= pd.read_csv('Month_Value_1.csv',nrows=50)
print(data.head())
```
```
data['Period']=pd.to_datetime(data['Period'])
data.set_index('Period',inplace=True)
plt.plot(data.index,data['Revenue'],label='Revenue')
plt.title("Company's Revenue")
plt.xlabel("Period")
plt.xticks(rotation=45)
plt.ylabel("Revenue")
plt.grid(True)
plt.legend()
plt.show()
```

# OUTPUT:
![Screenshot 2024-08-22 210534](https://github.com/user-attachments/assets/3ea88469-6776-4e88-9069-1527944b1a19)


# RESULT:
Thus we have created the python code for plotting the time series of given data.
