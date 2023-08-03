# Description
In this project, we tackle the problem of a low-cost supermarket chain trying to decide in which area of Madrid (Spain) they should open their new store in order to maximise the revenue. It is important to note that the city of Madrid consists of 21 districts and 131 neighbourhoods with great differences between them.

![image](https://github.com/nitindantu/Retail/assets/41870240/2fa7aae7-2c78-44a3-b48e-ce9cbeb0e6e6)

# Geospatial data
Since the plan is to target residential areas, we need to analyse the type of food venues present in
each neighbourhood. With the Foursquare API [2] we can explore the different food venues,
considering that a big density of bars and restaurants over very few supermarkets will most likely
refer to a business or recreational area where people don’t usually buy at supermarkets. In the other
hand, a large proportion of supermarkets over the rest of food venues might indicate it is a residential
area where people normally make their food shopping.
Before we can make use of the Foursquare API we need to convert the neighbourhood names into a
pair of latitude and longitude coordinates. We can query the Foursquare API using the HTTP GET
method on the explore endpoint indicating the geographical coordinates, venue categories and
radius.
The following figure shows the location of all the neighbourhoods within the city of Madrid, it is
important to remark that any areas and towns outside the city have not been considered for this
project.

![image](https://github.com/nitindantu/Retail/assets/41870240/bf2764a4-1e1f-4de9-8fe4-702ec66f5b26)


# Methodology

The neighbourhoods of Madrid are analysed with the purpose of finding the ideal location for a new
low-cost supermarket. We apply machine learning techniques such as k-means clustering to find
different clusters so that we could focus in only one type of neighbourhood (residential). Further data
such as population and market venues will be used to reduce the number of potential areas.


The following scatterplot represents the residential neighbourhoods considering the ratio people —
markets and the household income. The highlighted quadrant covers neighbourhoods with a
household income below average (since we are targeting working class areas) and a ratio of people
per market above average, making these neighbourhoods good candidates for the location of the
new store.

Since initially we don’t know how many different types of neighbourhood we can find in Madrid, we
are using the elbow method to obtain the optimal number (k) of clusters.
Although the figure below shows 3 as the optimal number of clusters, we are using 5 (the second
best k) since this way we can break down more the number of neighbourhoods that we are going to
analyse against the census data.

![image](https://github.com/nitindantu/Retail/assets/41870240/2d058ddf-15f4-4a42-87ed-ea6c4d9995fb)

With K-means algorithm we can group the 131 neighbourhoods into 5 clusters depending on the
most popular venues in those areas. Below we can visualise what are the most common venues and
the cluster (from 0 to 4) that has been assigned to each area.

![image](https://github.com/nitindantu/Retail/assets/41870240/7d669c62-9d7f-4f69-bb3c-9ca7f78c203f)

In order to name the different clusters it is necessary to explore the most representative venues in
the neighbourhoods of each cluster. Finally we come with the following representation:
![image](https://github.com/nitindantu/Retail/assets/41870240/580992d0-907e-43f7-bd33-cae4718c62cd)


# Result

![image](https://github.com/nitindantu/Retail/assets/41870240/fae6688f-f32f-449a-8837-df535e650ad1)

Above we can clearly see that Villaverde Alto looks the optimal neighbourhood since the household
income is clearly under average (around 26K €) and there are very few supermarkets for the amount
of population in the area.
However it would also be recommended to consider other similar areas such as Portazgo that is also
located on the bottom-right corner of the plot.
It is also interesting to mention that even though the low amount of existing supermarkets in
Mirasierra does clearly not cover the demand of the neighbourhood, it would be a convenient place
for a high class market since the household income there is at the very top.

# Conclusion
The neighbourhoods of Madrid were analysed with the purpose of finding the ideal location for a new
low-cost supermarket. We applied machine learning techniques such as k-means clustering to find
different clusters so that we could focus in only one type of neighbourhood (residential). Further data
such as population and market venues have been used to reduce the number of potential areas.
This project could be improved by only taking certain venue categories into consideration when
performing the clustering segmentation. We could for example identify the key types of venue that
define a residential area such as schools, pharmacies, small markets and corner shops, and the
types of venue that discard a residential area such as night clubs, theatres and so on. Another
improvement could be achieved by only handling certain groups of ages and social classes that
would normally shop in a supermarket.
Although this project focuses particularly in a low-cost supermarket, it could easily be amended for
any type of business and city, as long as the corresponding data are available to be included in the
analysis.
