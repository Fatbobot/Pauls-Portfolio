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
