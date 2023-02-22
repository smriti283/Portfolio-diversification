# Building a recommendation mode for diversification in a country’s product space portfolio


## Overview

The economy of a country is heavily influenced by the type of products it manufactures, imports and exports. While diversification of product space leads to economic growth, a country’s ability to enter into a new product market depends on its potential of developing the product with the required skills, manpower, capital and technology. In this project, we intend to study the connectedness (or disconnectedness) of products, in order to identify the country’s potential of product diversification and the likelihood/ feasibility of entering into a new product market or trade relations. 


We achieved this by first exploring the formation or lack of new trade links in a product space within a gap of 5 years, thereby analyzing existing links in 2014 and comparing with links in 2019. We then transformed the recommendation task into a classification task of trade by products amongst countries. By testing a combination of both traditional and advanced classification models using multiple features, based on gravity model approach and network graphs approach, we compared the performances of each model and approach. We found that while traditional models performed well on predicting future links, the complexities of the underlying dynamics of networks call for more advanced models that capture the network graph structures in order to make reliable predictions.


## Datasets

- [International Trade Data](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/H8SFD2): ATLAS of Economic Complexity Dataverse (Harvard University)
- GeoDist: Distance data between countries
- ArcGIS Datasets and Location data: Geospatial data for visualizations
          [World map shapefiles](https://hub.arcgis.com/datasets/2b93b06dc0dc4e809d3c8db5cb96ba69_0/explore)
          [World cities database](https://simplemaps.com/data/world-cities)
          

## Methods

1. Network visualization and basic exploratory analysis
2. Gravity Model and prediction by Classification
3. Augmented Gravity Model and prediction by Classification
4. Graph embeddings


## Results

