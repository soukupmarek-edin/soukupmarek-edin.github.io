---
layout: data_analysis_index
---

[back to main page](https://soukupmarek-edin.github.io/)

[back to data analysis page](https://soukupmarek-edin.github.io/data_analysis/data_analysis_main.html)


**Task 1:** Load the table `countries` and select only United Kingdom.

<details>
  <summary>Show solution</summary>
  
  ```
  source = "https://raw.githubusercontent.com/soukupmarek-edin/soukupmarek-edin.github.io/main/data_analysis/data/countries.csv"
  countries_df = pd.read_csv(source).loc["United Kingdom"]
  ```
  
</details>


[back to main page](https://soukupmarek-edin.github.io/)

[back to data analysis page](https://soukupmarek-edin.github.io/data_analysis/data_analysis_main.html)
