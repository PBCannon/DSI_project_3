# DRIVERS OF PROPERTY SALE PRICES 
KAGGLE AMES HOUSING DATASET link : https://www.kaggle.com/prevek18/ames-housing-dataset

**@PBCANNON/PROPERTY-SALEPRICE-PREDICTION-MODEL**

## PROJECT GOALS: 
•	Generate a machine learning model that predicts Home Sale Prices. 
•	Extract dollar values for positive and negative price drivers.
•	Use model to boost sale prices during an economic downturn.


## PART 1: MACHINE LEARNING
The Ames housing dataset contains 81 potential price drivers and the sale price for homes sold from 2006 to 2010. Extensive feature engineering and data cleaning was performed to make the dataset robust for machine learning. I first used Decision Trees & regularized linear regression models to identify the most important Fixed Drivers of sale price. Confirming online real estate resources, HOME SIZE, AGE & NEIGHBORHOOD were the main drivers found to positively influence price. The model though was not robust and could only predict prices at 80% confidence. I then used similar models and added the Renovatable Drivers to predict housing prices. Interestingly, the HOME QUALITY SCORE, SIZE OF EXTERIOR DECKS, EXTERIOR FINSHING, & GARAGE TYPE, were the main positive influencers of property sale price. By incorporating renovatable drivers, the model was then able to predict housing prices at 90% confidence.


## PART 2: EXTRACTING DOLLAR VALUES 

**Features That Increase Home Prices the Most**
| Positive Feature             | Dollar Value ($)|
|------------------------------|-----------------|
| Neighborhood_StoneBr         | 32880.12        |
| Neighborhood_NoRidge         | 23017.17        |
| Neighborhood_Crawfor         | 20195.57        |
| BsmtExposure_Gd              | 19080.46        |
| HouseStyle_2.5Fin            | 18713.02        |
| Neighborhood_NridgHt         | 15487.28        |
| Exterior1st_BrkFace          | 15358.40        |
| GarageType_BuiltIn           | 13802.29        |
| OverallQual                  | 11587.98        |
| BldgType_2fmCon              | 10985.58        |

| Negative Feature             | Dollar Value ($)|
|------------------------------|-----------------|
| BsmtExposure_No              | -9089.63        |
| Neighborhood_NWAmes          | -10411.27       |
| BldgType_Twnhs               | -12046.60       |
| BldgType_Duplex              | -15716.28       |
| KitchenQual_Gd               | -17834.89       |
| KitchenQual_Fa               | -19630.28       |
| BsmtQual_Fa                  | -21559.56       |
| BsmtQual_TA                  | -23375.19       |
| BsmtQual_Gd                  | -24297.04       |
| KitchenQual_TA               | -25280.95       |


**Value per unit added (unit of quality, sqft, per bathroom or age)**

|          Feature             | Dollar Value ($)|
|------------------------------|-----------------|
| OverallQual                  | 11587.98        |
| MasVnrArea                   | 26.39           |
| WoodDeckSF                   | 23.21           |
| OpenPorchSF                  | 62.59           |
| HalfBath                     | 4524.34         |
| home_age                     | -281.87         |




## PART 3: SIMULATING A MARKET DOWNTURN

The most important aspect of machine learning is the ability to use the model to derive business insights. The dataset provided contains data from the 2008 USA financial market crash. Therefore, a home bought pre-2008 and sold post-2008 would be selling at a loss. Using my model, I simulated how a home owner could take advantage of top drivers to sell their homes for a profit. 

|                                      | AS IS	                | WITH RENOVATIONS                               |
|--------------------------------------|------------------------|------------------------------------------------|
| PURCHASED PRICE (2006)               | $225,000.00	          | $225,000.00                                    |
| RENOVATION PRICE                     | N/A        	          | 200 SQFT DECK @ $20/SQFT = $5000               |
|                                      |                        |Basement Private Entrance = $15,000             |
|                                      |                        |Total  = $20,000                                |
| PREDICTED PRICE (2010)               | $225,764.32		        | $262,376.35                                    |
| INITIAL PRICE + INFLATION (2%)       | $260,000.00		        | $260,000.00                                    |             
| SALE – PURCHASED PRICE - RENOVATIONS | $764.32		            | $17,376                                        |

