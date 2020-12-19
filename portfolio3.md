In this example, we used the .groupby to create hierarchical indexing while creating a pandas dataframe, where the first "layer" of indexing uses .describe() abd the second "layer" are the selected columns 'flankers' and 'simon'. Crucially, I used the .describe on the 'rt' column so that the the first "layer" would have all the relevant information only on the 'rt' column. 


```python
df_cond_stats = pd.DataFrame(df.groupby(['flankers','simon'])['rt'].describe())

![image](https://user-images.githubusercontent.com/73757147/102678331-00cc3600-417e-11eb-9841-33ca38906e02.png)
```
