```
fig = plt.figure(figsize=[8, 12])
subplot_counter = 1

for ii in range(0,27,3):
    fig.add_subplot(3,3,subplot_counter)
    plt.imshow(fmri_zstat_data[:,:,ii],
               cmap='seismic', vmin= -8,
               vmax= 8)
    plt.axis('off')
    plt.tight_layout()
    subplot_counter += 1 
```
