# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 20/03/2025

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
```
/*
Developed by: M THEJESWARAN
Register Number: 212223240168
*/

import pandas as pd
import matplotlib.pyplot as plt

file_path = 'vgsales.csv' 
data = pd.read_csv(file_path)

data['Year'] = pd.to_datetime(data['Year'], format='%Y', errors='coerce')
data.set_index('Year', inplace=True)

data.sort_index(inplace=True)
plt.figure(figsize=(10, 6))
plt.plot(data.index, data['Global_Sales'], marker='o', linestyle='-', color='blue', label='Global Sales')

plt.title('Global Video Game Sales Over the Years')
plt.xlabel('Year')
plt.ylabel('Global Sales (Millions)')
plt.grid(True)
plt.legend()
plt.xticks(rotation=45)  # Rotate x-axis labels for better readability
plt.show()
```

# OUTPUT:
![download](https://github.com/user-attachments/assets/b457f222-9f10-4baa-8d06-496dece190bc)


# RESULT:
Thus we have created the python code for plotting the time series of given data.
