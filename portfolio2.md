 The first step is organizing which set of data values we want to organize by. In this case, we want the mean of the rt values but only the ones that correspond to the 'congruent' value in the column 'flankers'. Thus, we first use the .loc function to select the flankers column, and then use the '==' sign to indicate which values we want within the 'flankers' column. We use [] brackets because it is a Pandas dataframe.


```python
dat.loc[dat['flankers']=='congruent']['rt'].mean()

416.0478079416664
```
