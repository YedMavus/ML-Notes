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

### Writing Data

`A.to_csv("<filename>.csv")`

### Indexing

Pandas is optimised for table handling. Thus, it follows a row first, column second approach, which is opposite from that of native python.

`reviews.country` and `['reviews.country']` will output the column named "country", latter command working iff the table is a dictionary.


For indexing, `reviews['country'][0]` outputs the first row value of the col named country.
But more rigorously, pandas uses `reviews.iloc[0]` ie `.iloc[some number]` which has the row first approach. The numbers within `[]` supports slicing.
`reviews.iloc[:3, 0]` May be used if we want to avoid explicitly naming or referencing the columns.


Or not!


eg `reviews.loc[0, 'country']` is perfectly ok, but **notice the use of `.loc[]` and not `.iloc[]`**

`reviews.loc[:, ['taster_name', 'taster_twitter_handle', 'points']]`

##### Choosing between loc and iloc

When choosing or transitioning between loc and iloc, there is one "gotcha" worth keeping in mind, which is that the two methods use slightly different indexing schemes.

iloc uses the Python stdlib indexing scheme, where the first element of the range is included and the last one excluded. So 0:10 will select entries 0,...,9. 

loc, meanwhile, indexes inclusively. So 0:10 will select entries 0,...,10.

**Why the change?** Remember that loc can index any stdlib type: strings, for example. If we have a DataFrame with index values Apples, ..., Potatoes, ..., and we want to select "all the alphabetical fruit choices between Apples and Potatoes", then it's a lot more convenient to index `df.loc['Apples':'Potatoes']` than it is to index something like `df.loc['Apples', 'Potatoet']` (t coming after s in the alphabet).

This is particularly confusing when the DataFrame index is a simple numerical list, e.g. 0,...,1000. In this case `df.iloc[0:1000]` will return 1000 entries, while `df.loc[0:1000]` return 1001 of them! To get 1000 elements using loc, you will need to go one lower and ask for `df.loc[0:999]`.

Otherwise, the semantics of using loc are the same as those for iloc.

#### Checking Conditionals:

**MOST IMPORTANT: Pandas doesnt support usual python script `and` and `or`**

Only use operators `|` and  `&`  for OR and AND.

`reviews.loc[(reviews.country == 'Italy') | (reviews.points >= 90)]`

`reviews.loc[reviews.country.isin(['Italy', 'France'])]`

`reviews.loc[reviews.price.notnull()]`

