---
layout: data_analysis_index
---


**Task 1:** Load the table `countries` and select only United Kingdom.

<details>
  <summary>Show solution</summary>
  
  ```python
  source = "https://raw.githubusercontent.com/soukupmarek-edin/soukupmarek-edin.github.io/main/data_analysis/data/countries.csv"
  countries_df = pd.read_csv(source).loc["United Kingdom"]
  ```
  
</details>
