## ML Models and Data Preprocessing for AI4LS Hackathon

Hackathon - AI4LS Challenge #1: AI for Soil Health

### Soil Data Preprocessing
Scripts for precessing data from the Lucas Soil 2018 dataset are in folder:
- csv_processing

### Microbiome Data Processing
Only ~30/885 soil samples from the Microbiome Data provided by the Lucas 2018 dataset were processed 
They were processed using the Metabarcoding analysis using the PEMA tool: https://github.com/hariszaf/pema
Using the OTU- or ASV-tables generated by the Metabarcoding, it was attempted to use the number of OTUs calculate the Shannon diversity/Simpson diversity index to indicate the degree of soil biodiversity of samples. 
The related scripts and Metabarcoding results are in folder:
- microbiome_data_processing

### Training Prediction Models (Phy/Chem attributes <-> Land use)
Since we got limited amount of soil microbiome data, we only trained the prediction models which works on the relationship between land use/management and the traditional(physical/chemical) soil attributes. 
We attempted training approaches including SVM, Random Forest, and K-mean clustering. Among the approaches, SVM (SVC and SVR) used the most. 
The scripts of model training are organized mainly according to what is the model predicting, the folder are:
- prediction_attributes
- prediction_erosion
- prediction_impacted
- prediction_landuse
- relationship

### Future Work
- Phy/Chem Soil Attributes <-> Land Use
    - Discover importance of each physical/chemical attributes in affecting the soil health/predicting un-/managed 
    - Investigate better handling of the out-of-range measurements (eg. < LOD, NaN) => improve accuracy 
    - Attempt advanced AI model training approaches (eg. Neural networks) 
- Land Use <-> Soil Biodiversity <-> Phy/Chem Soil Attributes
    - Continue processing more Lucas microbiome samples 
    - Ways to better evaluation of the soil biodiversity (eg. Taxonomic Eveness, relative abundance ) 
    - Ways to use ML or AI computing power to find the relationship between physical/chemical attributes and soil biodiversity 