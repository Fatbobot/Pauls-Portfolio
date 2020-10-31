Here I used .groupby() and .describe() to output an organized table, outlining 4 variations between 2 variables, each with 2 corresponding variables.


```python
df_cond_stats = pd.DataFrame(df.groupby(['flankers','simon'])['rt'].describe())
```
