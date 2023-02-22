# Building a recommendation mode for diversification in a country’s product space portfolio


## Overview

The economy of a country is heavily influenced by the type of products it manufactures, imports and exports. While diversification of product space leads to economic growth, a country’s ability to enter into a new product market depends on its potential of developing the product with the required skills, manpower, capital and technology. In this project, we intend to study the connectedness (or disconnectedness) of products, in order to identify the country’s potential of product diversification and the likelihood/ feasibility of entering into a new product market or trade relations. 


We achieved this by first exploring the formation or lack of new trade links in a product space within a gap of 5 years, thereby analyzing existing links in 2014 and comparing with links in 2019. We then transformed the recommendation task into a classification task of trade by products amongst countries. By testing a combination of both traditional and advanced classification models using multiple features, based on gravity model approach and network graphs approach, we compared the performances of each model and approach. We found that while traditional models performed well on predicting future links, the complexities of the underlying dynamics of networks call for more advanced models that capture the network graph structures in order to make reliable predictions.


## Datasets

- [International Trade Data](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/H8SFD2): ATLAS of Economic Complexity Dataverse (Harvard University)
- GeoDist: Distance data between countries
- ArcGIS Datasets and Location data: Geospatial data for visualizations

          1. [World map shapefiles](https://hub.arcgis.com/datasets/2b93b06dc0dc4e809d3c8db5cb96ba69_0/explore)
          2. [World cities database](https://simplemaps.com/data/world-cities)
          

## Methods

1. Network visualization and basic exploratory analysis
2. Gravity Model and prediction by Classification
3. Augmented Gravity Model and prediction by Classification
4. Graph embeddings


## Results

### 1. Network visualization and basic exploratory analysis

Our raw dataset consists of trade flow details between 235 countries for 1218 numbers of products, translating to 5,467,612 trade records in 2014 and 5,404,920 trade records in 2019 between all countries and all products.


Therefore, to reduce the network complexity and to help draw initial insights, we decided to analyze a single product before progressing to the complete dataset with all products. After some deliberation, we chose the product **Coffee**, because of its perceived low dependability on other products which, we believed, would help us study the existing network of product trade in isolation.


We started with a basic network analysis on the given dataset, in order to quantify the node importance in the network and to understand network metrics such as degree, closeness centrality, betweenness centrality and pagerank centrality.


First, by comparing location_id & partner_id data between 2014 and 2019, new trade links were found.
Secondly, we created network data with exporting countries and importing countries as nodes and exported value as weight then calculated centrality. 
Lastly, we merged with world cities location data to map new trade links for all products in the USA and newly found links of coffee product.


Based on the above, network analysis was performed on two different datasets to draw insights on formation of new trade links between countries in 2019 as opposed to 2014:

- Trade flow data in 2014 and 2019 on coffee only;
- Trade flow data in 2014 and 2019 on all products


The trade flow network on both the above datasets were geo-visualized and the top 10 links were found.


Here is the result from "Coffee" data. The degree centrality calculated indicates that Canada and Vietnam have the highest density of connections, indicating that these are new emerging coffee exporting countries in 2019.


<img width="772" alt="Screen Shot 2023-02-20 at 10 30 31 PM" src="https://user-images.githubusercontent.com/78453405/220495084-2e31f255-e1bd-4aca-a40b-bdc58c8cfcbf.png">


Additionally, we found the top 10 countries that started new trades with the highest degree centrality, and this map shows America’s new network which has the highest value and its most exporting products.


