This for loop solved an issue where individual participant data needed to be preserved as individual (as to be accessed in case there were issues with an individual participant) , but had the ability to be concatenated later for group EDA. The structure provided here creates an empty list, in which any data processing is applied to, and is then appended to the empty list.


```python
processed_dataframes = []
for file in files:
    unprocessed_dataframe = pd.read_csv(file, sep='\t')
    (#insert cleaning here)
    processed_dataframes.append(unprocessed_dataframe)
```
