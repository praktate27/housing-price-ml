#Goal:
This project aims at predicting house prices (residential) in Ames, Iowa, USA. 

#Dataset:
Kaggle's Housing Data Set Knowledge Competition

#Factors that affect House Pricing:
*	Area of House
*	How old is the house
*	Location of the house
*	How close/far is the market
*	Connectivity of house location with transport
*	How many floors does the house have
*	What material is used in the construction
*	Water /Electricity availability
*	Play area / parks for kids (if any)
*	If terrace is available
*	If car parking is available
*	If security is available

#Data Exploration:

1. Output of Dataset shape
	
The train data has 1460 rows and 81 columns
----------------------------
The test data has 1459 rows and 80 columns

2. Missing Columns
	
['LotFrontage',
 'Alley',
 'MasVnrType',
 'MasVnrArea',
 'BsmtQual',
 'BsmtCond',
 'BsmtExposure',
 'BsmtFinType1',
 'BsmtFinType2',
 'Electrical',
 'FireplaceQu',
 'GarageType',
 'GarageYrBlt',
 'GarageFinish',
 'GarageQual',
 'GarageCond',
 'PoolQC',
 'Fence',
 'MiscFeature']

 3. Correlation score of columns with Sale Price

SalePrice -->      1.000000
OverallQual  -->   0.790982
GrLivArea -->      0.708624
GarageCars -->     0.640409
GarageArea -->     0.623431
TotalBsmtSF -->    0.613581
1stFlrSF -->       0.605852
FullBath -->       0.560664
TotRmsAbvGrd-->    0.533723
YearBuilt   -->    0.522897
YearRemodAdd-->    0.507101
GarageYrBlt-->     0.486362
MasVnrArea -->     0.477493
Fireplaces -->     0.466929
BsmtFinSF1 -->     0.386420
Name: SalePrice, dtype: float64, '\n')
----------------------
YrSold -->         -0.028923
OverallCond -->    -0.077856
MSSubClass -->     -0.084284
EnclosedPorch -->  -0.128578
KitchenAbvGr -->   -0.135907
Name: SalePrice, dtype: float64

4. Data Pre-processing

5. Feature Engineering

Most categorical variables have near-zero variance distribution. Near-zero variance distribution is when one of the categories in a variable has >90% of the values. We'll create some binary variables depicting the presence or absence of a category. The new features will contain 0 or 1 values.

6. Model training and Evaluation:

Here we are using 3 Algorithms, XGBoost, Neural Network, Lasso Regression.
We did RMSE on models and got following output on Kaggle score board:
* XGBoost : 0.12507
* Lasso Regression : 0.11859
* Neural Network : 1.35346

which means Lasso Regression is best fitted for our predictions.