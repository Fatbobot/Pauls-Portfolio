```
gavg = {}
for x, y in enumerate(conditions):
    val = mne.grand_average([evoked[subj][x] for subj in evoked.keys()])
    gavg.update({y: val})
gavg
```
