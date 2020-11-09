### Visualizing the DataFrame

#### From initial datafarme we created I am going to create a new Dataframe that shows all the countries where the total number of cases is more than 1000.

```python
import pandas as pd
import matplotlib.pyplot as plt

corona_data_df["Total Cases"] = corona_data_df["Cases"] + corona_data_df["New_cases"]
corona_data_df = corona_data_df[corona_data_df['Total Cases'] >=1000]
df = corona_data_df[['Country','Total Cases']]
df
```
<img src='coronavirus_cases.png' width="400"/>

#### Using the new DataFrame we created, i was able to visualize the total number of cases in each country

```python
df.plot(kind='bar', x='Country', y='Total Cases')

#Lable the x-axis of my graph
plt.xlabel('Country')

#Label the y-axis of the graph
plt.ylabel('Total Number of Cases')

#Give the graph a title 
plt.title('Total Number of COVID-19 Cases in each Country')

#Show graph
plt.show()
```
<img src='img1.png' width="650"/>

#### From the graph you can clearly see all the countries with more than a 1000 cases. 
#### You can also see that USA, Spain, China, Italy, Germany, Iran, and France have a high number of cases.