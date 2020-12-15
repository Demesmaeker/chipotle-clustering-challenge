# chipotle-clustering-challenge
becode, team challenge

### Must-have features

- A visualisation of the USA with chipotle locations
- Visualization of the different clusters
- Intrinsic analysis comparison of the clusters of at least 2 methods with varying arguments (using euclidian distance as criteria)
- A chosen centroid to live. Make your argument of why the chosen centroid is superior to others. Examples of arguments are:
    - highest density
    - greatest uninterrupted link of chipotle locations with smallest link-to-link distance
    - ...
- a Github page where results are visualized

## Steps
- [X]  Create the repository
- [X]  Install geopandas
- [X]  Plot the US map
- [X]  Visualize your data on this map
- [X]  Plot a dendogram of your data to help you decide the appropropriate clustering resolution
- [X]  Compare and analyse different clustering methods using intrinsic analysis to decide on a chosen method.
- [X]  Choose a centroid/adress to live
- [ ]  Publish your results to a Github page with an explanation of your method.

## Vizualisation

*Dataset "chipotle_stores" as "df"*

![chipotle_stores](/assets/img/chipotle_stores.png)

*Dataset "states" using geopandas*

![states](/assets/img/states.png)

At first we tried to draw the map of the states using geopandas...

![states_map](/assets/img/states_map.png)


...in order to be able to plot our points directly on the map.

![chipotle_map](/assets/img/chipotle_map.png)

## Data analysis

 Now we have to choosing only relevant states

 ![value_counts](/assets/img/value_counts.png)

Easy using this code 

 ```py
 df = df.groupby('state').filter(lambda x : len(x)>20)
 ```

And next ...

- Check number of invalid metric entries.
- Adjusting index

Our map looks much clearer like this

![chipotle_map](/assets/img/chipotle_map_2.png)

## Dendogram

![chipotle_map](/assets/img/dendogram.png)

## Let's cluster all of that

### Clusters
![cluster](https://user-images.githubusercontent.com/69633814/102191579-e5310900-3eb9-11eb-8877-50a2fa2ce0a7.png)

### Center of Clusters
![Snip20201215_8](https://user-images.githubusercontent.com/69633814/102198357-9471de00-3ec2-11eb-9c05-d8e1e568f8df.png)


### Clusters @ Califonia
![ca](https://user-images.githubusercontent.com/69633814/102198170-5b396e00-3ec2-11eb-8925-ae24b12720f4.png)

### Center of Clusters @ Califonia
![Snip20201215_7](https://user-images.githubusercontent.com/69633814/102198458-b1a6ac80-3ec2-11eb-8ef4-ac3f73a3c513.png)

