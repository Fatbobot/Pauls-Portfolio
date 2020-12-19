```
gavg = {}
for x, y in enumerate(conditions):
    val = mne.grand_average([evoked[subj][x] for subj in evoked.keys()])
    gavg.update({y: val})
gavg
________________________________________________________________________
Identifying common channels ...
Identifying common channels ...
Identifying common channels ...
Identifying common channels ...
{'Quiet/Control/Correct': <Evoked | 'Grand average (n = 20)' (average, N=20), [-0.19922, 1] sec, 64 ch, ~479 kB>,
 'Quiet/Violation/Correct': <Evoked | 'Grand average (n = 20)' (average, N=20), [-0.19922, 1] sec, 64 ch, ~479 kB>,
 'Noise/Control/Correct': <Evoked | 'Grand average (n = 20)' (average, N=20), [-0.19922, 1] sec, 64 ch, ~479 kB>,
 'Noise/Violation/Correct': <Evoked | 'Grand average (n = 20)' (average, N=20), [-0.19922, 1] sec, 64 ch, ~479 kB>}
```
