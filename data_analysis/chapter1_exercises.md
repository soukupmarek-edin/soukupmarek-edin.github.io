---
layout: data_analysis_index
---

[MAIN PAGE](https://soukupmarek-edin.github.io/) | [DATA ANALYSIS](https://soukupmarek-edin.github.io/data_analysis/data_analysis_main.html)

<!-- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/googlecolab/colabtools/blob/master/notebooks/colab-github-demo.ipynb) -->

**Task 1:** Load the table `countries` and select only United Kingdom.

<details>
  <summary>Show solution</summary>
  
  ```python
  source = "https://raw.githubusercontent.com/soukupmarek-edin/soukupmarek-edin.github.io/main/data_analysis/data/countries.csv"
  countries_df = pd.read_csv(source).loc["United Kingdom"]
  ```
  
</details>


[MAIN PAGE](https://soukupmarek-edin.github.io/) | [DATA ANALYSIS](https://soukupmarek-edin.github.io/data_analysis/data_analysis_main.html)
