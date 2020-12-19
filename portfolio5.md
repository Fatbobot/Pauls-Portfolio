In this example, the first line indicates the size of the figures, while the subplot counter is used within the loop to update and create new subplots. range() is used to indicate how many brain scans we want to go through(In this case 0-27, so all 27), and the 3 indicates we want to jump by three. We create the parameters for the subplot grid, then change some details using vmin/max and cmap to change the colour. In this image we indicate which regions in the brain show activation in response to a cetain stimulus.

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
![image](https://user-images.githubusercontent.com/73757147/102678513-6e2c9680-417f-11eb-8499-02a710ac1670.png)
