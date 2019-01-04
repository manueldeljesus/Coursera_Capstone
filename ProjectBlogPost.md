

# Santander and its neighborhoods

## Introduction

Santander is a small city in Northern Spain, that counts with slightly more than 200.000 inhabitants with an increasing old population and almost no industry or enterprise activity. The leading activity is the public administration and its university.

In the present blogpost, we briefly describe some of the results obtained in a study in which the city was cut into sections, and these compared among these through clustering. Such a tool could be used to detect imbalances in the distribution of activities that could be reduced by means of public policies.

The main conclusions of the study is that the small size, both in spatial extent and population, and the historic evolution of the city, already took care of a fair distribution of population and economic activity. However, the methodology proposed could be applied to other cities to explore possible imbalances and sketch remediation actions.

## Data and Methods

The data used for this project will be obtained from Foursquare ([https://es.foursquare.com/](https://foursquare.com/)) and from Santander Datos Abiertos ([http://datos.santander.es/)](http://datos.santander.es/)). Information on businesses will be obtained from Foursquare, while Santander Datos Abiertos will provide information about administrative boundaries, zip codes, parking spaces per area and population. All the data is combined into a dataframe that contains all the explicative variables for every section of the city. The so formed dataset will be the working dataset for the project.

A clustering algorithm will then be used to classify the different section into groups of similar sections. The total number of clusters will be selected in such a way that the clustering is compatible with the field experience, that is, ensuring that each cluster really represent a quantity and quality of activity that can be observed on the field. The information collected breaks the city of Santander into several sections that are shown in the figure below.

![Distribution of the different considered sections in the city of Santander](SectionDistributionSantander.png)

## Results

The Foursquare API has been used to collect the information about the different venues present in the different sections of the city of Santander. Every section is assigned a vector that summarizes its characteristics which contains the 10 most important venues of the area. Different section of the city have been clustered based on the most important venues, obtaining the classification shown in the following figure.

![Distribution of the different considered sections in the city of Santander](ClusterDistributionSantander.png)

The most present cluster group is cluster number 3 (in cyan in the image above). This kind of section can be found all over the city, without any privileged area. This extensive area coverage also concentrates most of the population of the city as is shown in the figure below.

![Distribution of population per cluster type](PopulationPerCluster.png)

This cluster is characterized by the presence of convenience stores, supermarkets and small bars. It contains most of the housing spaces in the city.

Another important cluster type is number 1 (in purple in the figures) which characterizes most of the commercial areas, with a wide range of restaurants and other services such as pharmacies. This cluster type is the second in importance regarding population.

Cluster 2, in navy, contains most of the bar and pub areas of the city. These areas tend to have some problems related to noise, due to nocturnal activity, and for that reason it contains a small portion of the population.

Clusters 4, 5 and 6 contain most of the services of the city: gift shops, comics shops, clothing shops, etc. They are the least populated clusters mainly due to the fact that are in areas where only office buildings are present and thus, no housing is present.

The analysis of results shows that there is not a clear pattern that explains the distribution of services and population in the city. It may be due to the small size of the city, but services do not seem to properly cluster in space. Only the bars and pubs seem to be properly clusterized in a specific spatial regions for the rest of the services are interspersed.

It seem that the historic evolution of the city is stronger for explaining the distribution of services and venues that a real socio-economic dynamics. Indeed, Santander was destroyed by a big fire in 1941 that forced the city to reinvent itself. Many streets were changed and new neighborhoods were created. Commercial activity was concentrated in the city center, and the old uses were displaced to new areas.

## Conclusions

Small cities like Santander seem to be a example for the application of regressions techniques to the explanation of their dynamics. The small number of population and commercial activity means that most of the sections appear as outliers, due to the fact that very little areas are alike, there is always something that makes a section very different to other one.

In any case, the classification carried out clearly shows that most of the housing sections are surrounded by commercial areas that offer most of the services required; therefore making it difficult to show possible ways to improve the city.

The methodology however may be applied to larger cities, where the larger amount of population and the larger space to cover, can generate opportunities to improve the presence of important commercial activities for the section or the neighborhood.
