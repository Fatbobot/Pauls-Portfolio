```
sns.catplot(kind = 'box', data = df_means, y= 'value', x = 'background', hue ='sen_type',
                 palette = "colorblind")
plt.title('ERP Amplitude, Sentence Type, and Background')
plt.xlabel('Background')
plt.ylabel('Mean ERP Amplitude')
plt.show()
```
