# Monitoring illegal mining in India
Illegal mining is a concern worldwide with its wide-ranging effects on the environment such as biodiversity loss, loss of an ecosystem, toxic chemicals released into the environment, human displacement etc. This created a need to monitor illicit mining. Although with respect to India, the MoEFCC is responsible to grant clearances for mining but there are mines which are still operating without official paperwork. India has a large landscape, and it is not feasible to track these mines by site visits. With the advent of remote sensing techniques, it provides us with a cost-effective tool to monitor these mines spatially and temporally with fine resolution. Hence, we propose a remote sensing method to monitor illegal mining in India.  

The method employs a deep learning model trained on satellite images of a dataset released by [1] containing surface mines globally. Given an input satellite image, the model is used to predict mine/ non-mine for each pixel. See figure below: 

![Image of Mine using RGB bands](https://github.com/ashishraj615/Model_Predictions/blob/main/RGB_Mine.jpeg)
![Image of prediction](https://github.com/ashishraj615/Model_Predictions/blob/main/Mine_prediction.jpeg)




Using this model, it now becomes feasible to monitor mines which got environment clearances by MoEFCC. The MoEFCC is a Govt. Of India portal, that grants environment clearance for mining proposal. The information about all the mining proposals ranging from 2006-2016 in this portal was datafied by [2]. This data was also complemented by a dataset from Indian Bureau of Mines. Thus, curating a rich dataset about all the mining proposals with each mine having variables such as clearance date, location of mine, type of mineral, mine production capacity, mine area, lease grant date etc.  

The dataset [2] contains location of mine in terms of a single (lat,long) coordinate which makes it difficult to delineate the area used by the mine. In order to delineate the area used by the mine, the above model was used. Thus, creating a bounding box around the mine coordinate which can be seen as a boundary outside which the probability of mine existence is much lower. OSM being driven by ethics of open data, crowdsourcing and local knowledge can play a vital role in monitoring these mines after their date of clearances. By providing delineated boundaries of mines to OSM community, contributors can further annotate the extent of mine. The objective is to add new mining locations to OSM, given a candidate set of location polygons generated from [2]. We would like the OSM community to examine these locations and validate their correctness, and the final valid locations can be added to OSM.   

We would be highly grateful to the OSM community for their collaboration in monitoring of illegal mines in India so that govt.  can take further steps to regarding the same.  

Link to the project report along with accuracy details of model: https://drive.google.com/file/d/1UyJPbSF8LYi-16pKNR0eat1saG-fXcu5/view?usp=sharing 

References

1. Maus, V., Giljum, S., Gutschlhofer, J. et al. A global-scale data set of mining areas. Sci Data 7, 289 (2020). https://doi.org/10.1038/s41597-020-00624-w

2. Pande, Rohini; Sudarshan, Anant, 2019, "Harnessing transparency initiatives to improve India's environmental clearance process for the mineral mining sector", https://doi.org/10.7910/DVN/NF5GZY, Harvard Dataverse, V1
