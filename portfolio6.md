```
sns.catplot(kind = 'box', data = df_means, y= 'value', x = 'background', hue ='sen_type',
                 palette = "colorblind")
plt.title('ERP Amplitude, Sentence Type, and Background')
plt.xlabel('Background')
plt.ylabel('Mean ERP Amplitude')
plt.show()
```
![image](https://user-images.githubusercontent.com/73757147/102678852-6cfc6900-4181-11eb-8286-295a56e85684.png)
