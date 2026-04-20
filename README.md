# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 20-04-2026

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
from matplotlib import pyplot as plt
import pandas as pd

df = pd.read_csv("/content/DailyDelhiClimateTest.csv")
df.head()

df['date'] = pd.to_datetime(df['date'])
df.dtypes

df.set_index('date', inplace=True)
df_resampled = df['humidity'].resample('D').interpolate()
df_resampled.plot(kind = 'line',label='Humidity',color = 'black')
plt.title('Humidity vs Date')
plt.xlabel('Date')
plt.ylabel('Humidity')
plt.legend()
plt.grid(True)
plt.show()

```






# OUTPUT:

<img width="458" height="331" alt="image" src="https://github.com/user-attachments/assets/47f9ea54-e1ae-465e-b3ad-a628cba5cea4" />







# RESULT:
Thus we have created the python code for plotting the time series of given data.
