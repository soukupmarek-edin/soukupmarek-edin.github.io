---
layout: data_analysis_index
---

[MAIN PAGE](https://soukupmarek-edin.github.io/) | [DATA ANALYSIS](https://soukupmarek-edin.github.io/data_analysis/data_analysis_main.html)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1z_S9y6VA5M3uab2UZJNhrPaUSsMbA2VZ?usp=sharing)

### Imports

```{python}
import pandas as pd
```

### Data load and description

**Task 1:** Load `countries` and select the United Kingdom only. Save this DataFrame as `uk_df`. The source of the data is 
[HERE](https://raw.githubusercontent.com/soukupmarek-edin/soukupmarek-edin.github.io/main/data_analysis/data/countries.csv).

<details>
  <summary>Show solution</summary>
  
  ```python
source = "https://raw.githubusercontent.com/soukupmarek-edin/soukupmarek-edin.github.io/main/data_analysis/data/countries.csv"

# option 1
uk_df = pd.read_csv(source, index_col='country').loc["United Kingdom"].reset_index()

# option 2
uk_df = pd.read_csv(source).query("country == 'United Kingdom'")

# option 3
uk_df = pd.read_csv(source)
uk_df = uk_df[uk_df['country']=='United Kingdom']
  ```
  
</details>

* * *

**Task 2:** Drop the `country` column, which is not of any use anymore, and set `year` as index.

<details>
  <summary>Show solution</summary>
  
  ```python
uk_df = uk_df.drop('country', 1).set_index('year')
  ```
  
</details>

* * *

**Task 3:** Display the number of rows and columns in the table.

<details>
  <summary>Show solution</summary>
  
  ```python
uk_df.shape
  ```
  
</details>

* * *

**Task 4:** Display the upper 10 rows and the lower 10 rows.

<details>
  <summary>Show solution</summary>
  ```python
print(uk_df.head())
print(uk_df.tail())
  ```
</details>

* * *

**Task 5:** Display the data types of the columns in the table.

<details>
  <summary>Show solution</summary>
  
  ```python
uk_df.info()
  ```
  
</details>

* * *

**Task 6:** Display the mean, standard deviation, count, minimum, maximum and quartiles.

<details>
  <summary>Show solution</summary>
  
  ```python
uk_df.describe()
  ```
  
</details>

* * *

**Task 7:** Find the number of missing data in every column.

<details>
  <summary>Show solution</summary>
  
  ```python
uk_df.isna().sum()
  ```
  
</details>

* * *

**Task 8:** Drop all rows with any missing values.

<details>
  <summary>Show solution</summary>
  
  ```python
uk_df.dropna(inplace=True)
  ```
  
</details>

* * *

### Working with columns

**Task 9:** Create a new column `GDP_pc` containing GDP per capita. Round the column.

<details>
  <summary>Show solution</summary>
  
  ```python
# option 1
uk_df['GDP_pc'] = uk_df['GDP'] / uk_df['population']

# option 2
uk_df = uk_df.assign(GDP_pc = uk_df.GDP / uk_df.population)

# rounding
uk_df['GDP_pc'] = uk_df['GDP_pc'].round()
  ```
  
</details>

* * *


[MAIN PAGE](https://soukupmarek-edin.github.io/) | [DATA ANALYSIS](https://soukupmarek-edin.github.io/data_analysis/data_analysis_main.html)











