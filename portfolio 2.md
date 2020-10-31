Here I took advantage of "==" to locate the mean of values in a column that corresponded to values in another column.


```python
dat.loc[dat['flankers']=='congruent']['rt'].mean()
```
