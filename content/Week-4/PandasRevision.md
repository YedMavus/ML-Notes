---
title: "Pandas Revision"
date: 2022-03-27 00:00:00 +0000
katex: true
---


# Pandas

First and foremost `import pandas as pd`

pandas consists of two core objects: **DataFrame** and the **Series**

Dataframe can be thought of as a table of diff values., while the Series can be thought of as a single column of a table consisting of a list of stuff.

### DataFrame

```
pd.DataFrame({'Bob': ['I liked it.', 'It was awful.'], 
              'Sue': ['Pretty good.', 'Bland.']},
             index=['Product A', 'Product B'])
```

### Series

```
pd.Series([30, 35, 40], index=['2015 Sales', '2016 Sales', '2017 Sales'], name='Product A')
```

### Reading Data

`A = pd.read_csv("<some file path>",  index_col=0)`
  Where A is a DataFrame. ` index_col=0` indicates that the first column of the data is the index of rows, so is not actually data to be considered in the body, only as heading
  
`A.shape()` and `A.head()` give the dimension and top 10 entries respectively to let us wrap our head round the data.
