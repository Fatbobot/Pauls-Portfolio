This is an example using MNE topomaps. The purpose of topomaps is to show electrode data on a persons head at a specific time interval which can be specified in the arguments of .plot_topomap(). First we start by creating a list with times that we are interested in investigating. Next we forloop through a list of items that we want to create topomaps out of and specify relevant arguments. The product is an organized array of electrode data visualized in heatmap style.

```
times = [.100, .200, .300, .400, .500, .600, .700, .800, .900]
for cond in gavg_diff:
    gavg_diff[cond].plot_topomap(times,
                            average=.100,
                           vmin= -3,
                           vmax= 3)
    plt.show()
    Cz_idx = gavg['Quiet/Control/Correct'].ch_names.index('Cz')

mne.viz.plot_compare_evokeds(gavg_diff[cond], picks=Cz_idx)
```
![image](https://user-images.githubusercontent.com/73757147/102679294-1abd4700-4185-11eb-9124-d37c4c8f6377.png)
