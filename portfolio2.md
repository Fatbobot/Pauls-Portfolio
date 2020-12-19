![image](https://user-images.githubusercontent.com/73757147/102678278-bea2f480-417d-11eb-92a3-0e89ff7d93eb.png)

The first step is organizing which set of data values we want to organize by in the above dataframe. In this case, we want the mean of the rt values but only the ones that correspond to the 'congruent' value in the column 'flankers'. Thus, we first use the .loc function to select the flankers column, and then use the '==' sign to indicate which values we want within the 'flankers' column. We use [] brackets because it is a Pandas dataframe.


```python
dat.loc[dat['flankers']=='congruent']['rt'].mean()
__________________________________________________
416.0478079416664
```
