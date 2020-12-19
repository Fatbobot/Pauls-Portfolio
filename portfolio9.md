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
