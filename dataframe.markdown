### Creating DataFrame from a .csv file 

#### The .csv file contains the number of covid 19 cases in the world as of April 1st 2020, it has the following columns (country, number of cases, new cases, deaths, new deaths, transmission, days last reported, level, date last updated, travel restriction)


```python
import pandas as pd
import matplotlib.pyplot as plt

corona_data_df = pd.read_csv("coronavirus_merged_sources_Apr12020.csv")
```

```python
print(corona_data_df)
```

![](corona_head.png)