In this example, we use enumerate in combination with a forloop to loop through a list of lists. Conclusively, we append it to an empty list we created it called 'df_list', but notably at the end we concatenate all the new pandas dataframes into a singular data frame. Using the enumerate function, we preserve the 'name' of items within the list of lists, while also giving them an index to reference within the loop.
```
df_list = []
for suj in subjects:
    for a,b, in enumerate(conditions):
        z = evoked[suj][a].to_data_frame( time_format='ms', picks= Cz_idx, long_format=True)
        df_list.append(z)
        z['subject'],z['condition']= suj, b
df= pd.concat(df_list)
df.sample(10)
```
![image](https://user-images.githubusercontent.com/73757147/102680401-1fd2c400-418e-11eb-8a66-e0f87fa1f772.png)
