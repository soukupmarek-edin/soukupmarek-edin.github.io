---
layout: data_analysis_index
---

[MAIN PAGE](https://soukupmarek-edin.github.io/) | [DATA ANALYSIS](https://soukupmarek-edin.github.io/data_analysis/data_analysis_main.html)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1z_S9y6VA5M3uab2UZJNhrPaUSsMbA2VZ?usp=sharing)

**Task 1:** Load `countries` and select the United Kingdom only. The source of the data is 
[HERE](https://raw.githubusercontent.com/soukupmarek-edin/soukupmarek-edin.github.io/main/data_analysis/data/countries.csv).

<details>
  <summary>Show solution</summary>
  
  ```python
source = "https://raw.githubusercontent.com/soukupmarek-edin/soukupmarek-edin.github.io/main/data_analysis/data/countries.csv"
countries_df = pd.read_csv(source, index_col='country').loc["United Kingdom"]
  ```
  
</details>


[MAIN PAGE](https://soukupmarek-edin.github.io/) | [DATA ANALYSIS](https://soukupmarek-edin.github.io/data_analysis/data_analysis_main.html)











