# Project 2 - Ames Housing Data and Kaggle Challenge

## Problem Statement
Primary objective of the project is to predict sale prices of the house for the sellers and prospective buyers to optimize the house buying process. The goals of this project are following:
* Analyze the provided dataset,
* Understand the relationship between different features through EDA, 
* clean the data through deletion and imputing the data
* Creating graphs to visually understand the relationship between features.
* Develop a regression model which can effectively predict housing prices based on certain parameters. 


## Provided Dataset
The dataset set used here is Ames Housing dataset. There are two parts in data. 
* train.csv: This is the input training data, already has sale price of the house and requires cleaning
* test.csv: This is the input test data which requires cleaning and needs the housing price prediction.
 

The training data is not clean. So first the cleaning of this dataset was done,to eventually find no nulls. Certain columns were dropped in this process such as Alley which had to many missing values.

### Data Dictionary

   SalePrice - the property's sale price in dollars. This is the target variable.
   
   MSSubClass: The building class
       20 1-STORY 1946 & NEWER ALL STYLES
       30 1-STORY 1945 & OLDER
       40 1-STORY W/FINISHED ATTIC ALL AGES
       45 1-1/2 STORY - UNFINISHED ALL AGES
       50 1-1/2 STORY FINISHED ALL AGES
       60 2-STORY 1946 & NEWER
       70 2-STORY 1945 & OLDER
       75 2-1/2 STORY ALL AGES
       80 SPLIT OR MULTI-LEVEL
       85 SPLIT FOYER
       90 DUPLEX - ALL STYLES AND AGES
       120 1-STORY PUD (Planned Unit Development) - 1946 & NEWER
       150 1-1/2 STORY PUD - ALL AGES
       160 2-STORY PUD - 1946 & NEWER
       180 PUD - MULTILEVEL - INCL SPLIT LEV/FOYER
       190 2 FAMILY CONVERSION - ALL STYLES AND AGES
       
   MSZoning: Identifies the general zoning classification of the sale.
       A Agriculture
       C Commercial
       FV Floating Village Residential
       I Industrial
       RH Residential High Density
       RL Residential Low Density
       RP Residential Low Density Park
       RM Residential Medium Density
       
   LotFrontage: Linear feet of street connected to property
   
   LotArea: Lot size in square feet
   
   Street: Type of road access to property
       Grvl Gravel
       Pave Paved
       
   Alley: Type of alley access to property
       Grvl Gravel
       Pave Paved
       NA No alley access
       
   LotShape: General shape of property
       Reg Regular
       IR1 Slightly irregular
       IR2 Moderately Irregular
       IR3 Irregular
       
   LandContour: Flatness of the property
       Lvl Near Flat/Level
       Bnk Banked - Quick and significant rise from street grade to building
       HLS Hillside - Significant slope from side to side
       Low Depression
       
   Utilities: Type of utilities available
       AllPub All public Utilities (E,G,W,& S)
       NoSewr Electricity, Gas, and Water (Septic Tank)
       NoSeWa Electricity and Gas Only
       ELO Electricity only
       
   LotConfig: Lot configuration
       Inside Inside lot
       Corner Corner lot
       CulDSac Cul-de-sac
       FR2 Frontage on 2 sides of property
       FR3 Frontage on 3 sides of property
       
   LandSlope: Slope of property
       Gtl Gentle slope
       Mod Moderate Slope
       Sev Severe Slope
       
   Neighborhood: Physical locations within Ames city limits
       Blmngtn Bloomington Heights
       Blueste Bluestem
       BrDale Briardale
       BrkSide Brookside
       ClearCr Clear Creek
       CollgCr College Creek
       Crawfor Crawford
       Edwards Edwards
       Gilbert Gilbert
       GrnHill Green Hill
       IDOTRR Iowa DOT and Rail Road
       MeadowV Meadow Village
       Mitchel Mitchell
       Names North Ames
       NoRidge Northridge
       NPkVill Northpark Villa
       NridgHt Northridge Heights
       NWAmes Northwest Ames
       OldTown Old Town
       SWISU South & West of Iowa State University
       Sawyer Sawyer
       SawyerW Sawyer West
       Somerst Somerset
       StoneBr Stone Brook
       Timber Timberland
       Veenker Veenker
       
   Condition1: Proximity to main road or railroad
       Artery Adjacent to arterial street
       Feedr Adjacent to feeder street
       Norm Normal
       RRNn Within 200' of North-South Railroad
       RRAn Adjacent to North-South Railroad
       PosN Near positive off-site feature--park, greenbelt, etc.
       PosA Adjacent to postive off-site feature
       RRNe Within 200' of East-West Railroad
       RRAe Adjacent to East-West Railroad
       
   Condition2: Proximity to main road or railroad (if a second is present)
       Artery Adjacent to arterial street
       Feedr Adjacent to feeder street
       Norm Normal
       RRNn Within 200' of North-South Railroad
       RRAn Adjacent to North-South Railroad
       PosN Near positive off-site feature--park, greenbelt, etc.
       PosA Adjacent to postive off-site feature
       RRNe Within 200' of East-West Railroad
       RRAe Adjacent to East-West Railroad
       
   BldgType: Type of dwelling
       1Fam Single-family Detached
       2FmCon Two-family Conversion; originally built as one-family dwelling
       Duplx Duplex
       TwnhsE Townhouse End Unit
       TwnhsI Townhouse Inside Unit
       
   HouseStyle: Style of dwelling
       1Story One story
       1.5Fin One and one-half story: 2nd level finished
       1.5Unf One and one-half story: 2nd level unfinished
       2Story Two story
       2.5Fin Two and one-half story: 2nd level finished
       2.5Unf Two and one-half story: 2nd level unfinished
       SFoyer Split Foyer
       SLvl Split Level
       
   OverallQual: Overall material and finish quality
       10 Very Excellent
       9 Excellent
       8 Very Good
       7 Good
       6 Above Average
       5 Average
       4 Below Average
       3 Fair
       2 Poor
       1 Very Poor
       
   OverallCond: Overall condition rating
       10 Very Excellent
       9 Excellent
       8 Very Good
       7 Good
       6 Above Average
       5 Average
       4 Below Average
       3 Fair
       2 Poor
       1 Very Poor
       
   YearBuilt: Original construction date
   
   YearRemodAdd: Remodel date (same as construction date if no remodeling or additions)
   
   RoofStyle: Type of roof
       Flat Flat
       Gable Gable
       Gambrel Gabrel (Barn)
       Hip Hip
       Mansard Mansard
       Shed Shed
       
   RoofMatl: Roof material
       ClyTile Clay or Tile
       CompShg Standard (Composite) Shingle
       Membran Membrane
       Metal Metal
       Roll Roll
       Tar&Grv Gravel & Tar
       WdShake Wood Shakes
       WdShngl Wood Shingles
       
   Exterior1st: Exterior covering on house
       AsbShng Asbestos Shingles
       AsphShn Asphalt Shingles
       BrkComm Brick Common
       BrkFace Brick Face
       CBlock Cinder Block
       CemntBd Cement Board
       HdBoard Hard Board
       ImStucc Imitation Stucco
       MetalSd Metal Siding
       Other Other
       Plywood Plywood
       PreCast PreCast
       Stone Stone
       Stucco Stucco
       VinylSd Vinyl Siding
       Wd Sdng Wood Siding
       WdShing Wood Shingles
       
   Exterior2nd: Exterior covering on house (if more than one material)
       AsbShng Asbestos Shingles
       AsphShn Asphalt Shingles
       BrkComm Brick Common
       BrkFace Brick Face
       CBlock Cinder Block
       CemntBd Cement Board
       HdBoard Hard Board
       ImStucc Imitation Stucco
       MetalSd Metal Siding
       Other Other
       Plywood Plywood
       PreCast PreCast
       Stone Stone
       Stucco Stucco
       VinylSd Vinyl Siding
       Wd Sdng Wood Siding
       WdShing Wood Shingles
       
   MasVnrType: Masonry veneer type
       BrkCmn Brick Common
       BrkFace Brick Face
       CBlock Cinder Block
       None None
       Stone Stone
       
   MasVnrArea: Masonry veneer area in square feet
   
   ExterQual: Exterior material quality
       Ex Excellent
       Gd Good
       TA Average/Typical
       Fa Fair
       Po Poor
       
   ExterCond: Present condition of the material on the exterior
       Ex Excellent
       Gd Good
       TA Average/Typical
       Fa Fair
       Po Poor
       
   Foundation: Type of foundation
       BrkTil Brick & Tile
       CBlock Cinder Block
       PConc Poured Contrete
       Slab Slab
       Stone Stone
       Wood Wood
       
   BsmtQual: Height of the basement
       Ex Excellent (100+ inches)
       Gd Good (90-99 inches)
       TA Typical (80-89 inches)
       Fa Fair (70-79 inches)
       Po Poor (<70 inches)
       NA No Basement
       
   BsmtCond: General condition of the basement
       Ex Excellent
       Gd Good
       TA Typical - slight dampness allowed
       Fa Fair - dampness or some cracking or settling
       Po Poor - Severe cracking, settling, or wetness
       NA No Basement
       
   BsmtExposure: Walkout or garden level basement walls
       Gd Good Exposure
       Av Average Exposure (split levels or foyers typically score average or above)
       Mn Mimimum Exposure
       No No Exposure
       NA No Basement
       
   BsmtFinType1: Quality of basement finished area
       GLQ Good Living Quarters
       ALQ Average Living Quarters
       BLQ Below Average Living Quarters
       Rec Average Rec Room
       LwQ Low Quality
       Unf Unfinshed
       NA No Basement
       
   BsmtFinSF1: Type 1 finished square feet
   
   BsmtFinType2: Quality of second finished area (if present)
       GLQ Good Living Quarters
       ALQ Average Living Quarters
       BLQ Below Average Living Quarters
       Rec Average Rec Room
       LwQ Low Quality
       Unf Unfinshed
       NA No Basement
       
   BsmtFinSF2: Type 2 finished square feet
   
   BsmtUnfSF: Unfinished square feet of basement area
   
   TotalBsmtSF: Total square feet of basement area
   
   Heating: Type of heating
       Floor Floor Furnace
       GasA Gas forced warm air furnace
       GasW Gas hot water or steam heat
       Grav Gravity furnace
       OthW Hot water or steam heat other than gas
       Wall Wall furnace
       
   HeatingQC: Heating quality and condition
       Ex Excellent
       Gd Good
       TA Average/Typical
       Fa Fair
       Po Poor
       
   CentralAir: Central air conditioning
       N No
       Y Yes
       
   Electrical: Electrical system
       SBrkr Standard Circuit Breakers & Romex
       FuseA Fuse Box over 60 AMP and all Romex wiring (Average)
       FuseF 60 AMP Fuse Box and mostly Romex wiring (Fair)
       FuseP 60 AMP Fuse Box and mostly knob & tube wiring (poor)
       Mix Mixed
       
   1stFlrSF: First Floor square feet
   
   2ndFlrSF: Second floor square feet
   
   LowQualFinSF: Low quality finished square feet (all floors)
   
   GrLivArea: Above grade (ground) living area square feet
   
   BsmtFullBath: Basement full bathrooms
   
   BsmtHalfBath: Basement half bathrooms
   
   FullBath: Full bathrooms above grade
   
   HalfBath: Half baths above grade
   
   Bedroom: Number of bedrooms above basement level
   
   Kitchen: Number of kitchens
   
   KitchenQual: Kitchen quality
       Ex Excellent
       Gd Good
       TA Typical/Average
       Fa Fair
       Po Poor
   TotRmsAbvGrd: Total rooms above grade (does not include bathrooms)
   
   Functional: Home functionality rating
       Typ Typical Functionality
       Min1 Minor Deductions 1
       Min2 Minor Deductions 2
       Mod Moderate Deductions
       Maj1 Major Deductions 1
       Maj2 Major Deductions 2
       Sev Severely Damaged
       Sal Salvage only
       
   Fireplaces: Number of fireplaces
   
   FireplaceQu: Fireplace quality
       Ex Excellent - Exceptional Masonry Fireplace
       Gd Good - Masonry Fireplace in main level
       TA Average - Prefabricated Fireplace in main living area or Masonry Fireplace in basement
       Fa Fair - Prefabricated Fireplace in basement
       Po Poor - Ben Franklin Stove
       NA No Fireplace
       
   GarageType: Garage location
       2Types More than one type of garage
       Attchd Attached to home
       Basment Basement Garage
       BuiltIn Built-In (Garage part of house - typically has room above garage)
       CarPort Car Port
       Detchd Detached from home
       NA No Garage
       
   GarageYrBlt: Year garage was built
   
   GarageFinish: Interior finish of the garage
       Fin Finished
       RFn Rough Finished
       Unf Unfinished
       NA No Garage
       
   GarageCars: Size of garage in car capacity
   
   GarageArea: Size of garage in square feet
   
   GarageQual: Garage quality
       Ex Excellent
       Gd Good
       TA Typical/Average
       Fa Fair
       Po Poor
       NA No Garage
       
   GarageCond: Garage condition
       Ex Excellent
       Gd Good
       TA Typical/Average
       Fa Fair
       Po Poor
       NA No Garage
       
   PavedDrive: Paved driveway
       Y Paved
       P Partial Pavement
       N Dirt/Gravel
       
   WoodDeckSF: Wood deck area in square feet 
   
   OpenPorchSF: Open porch area in square feet
   
   EnclosedPorch: Enclosed porch area in square feet
   
   3SsnPorch: Three season porch area in square feet
   
   ScreenPorch: Screen porch area in square feet
   
   PoolArea: Pool area in square feet
   
   PoolQC: Pool quality
       Ex Excellent
       Gd Good
       TA Average/Typical
       Fa Fair
       NA No Pool
       
   Fence: Fence quality
       GdPrv Good Privacy
       MnPrv Minimum Privacy
       GdWo Good Wood
       MnWw Minimum Wood/Wire
       NA No Fence
       
   MiscFeature: Miscellaneous feature not covered in other categories
       Elev Elevator
       Gar2 2nd Garage (if not described in garage section)
       Othr Other
       Shed Shed (over 100 SF)
       TenC Tennis Court
       NA None
       
   MiscVal: $Value of miscellaneous feature
   
   MoSold: Month Sold
   
   YrSold: Year Sold
   
   SaleType: Type of sale
       WD Warranty Deed - Conventional
       CWD Warranty Deed - Cash
       VWD Warranty Deed - VA Loan
       New Home just constructed and sold
       COD Court Officer Deed/Estate
       Con Contract 15% Down payment regular terms
       ConLw Contract Low Down payment and low interest
       ConLI Contract Low Interest
       ConLD Contract Low Down
       Oth Other


## Output
As part of the project, I have produced multiple artifacts. 

* Jupyter Notebooks
*  1. Saba_Project_2_EDA: EDA, Imputation and visualizations for the train data. The result is saved as `cleaned_train_data.csv`
*  2. Saba_project_2_EDA_test_data: This does basic cleaning of test data as was done for train data, the result is saved in `Test_Data_Cleaned_All_Features`
*  3.Feature_Engineering: This does feature engineering of the test and train data and builds regression models too. The resulting datasets are saved as-`submission1.csv`,`submission2.csv` and `submission3.csv`


*  DataSet including results of various regressions:
   *  `cleaned_train_data.csv`
   *  `Test_Data_Cleaned_All_Features`
   *  `submission1.csv`
   *  `submission2.csv`
   *  `submission3.csv`
 
 
Exhaustive cleaning has been done for the 'train.csv' to aid us in building any number of models in the future. I have dropped any column which has more than 50% missing values and used interpolation & imputation to drive the values for the rest missing row values.  
Scatter plots and other relevant plots have been drawn for all the features against the sale price to visually understand the relationship between a column and sale price of the house.

Identify and bucketize the columns into different datatypes ['nominal', 'ordinal', 'discrete', 'continuos']


## Models
Models employed are:
1. Linear Regression
2. RidgeCV
3. LassoCV
4. LassoCV with optimal alpha
5. RidgeCV with optimal alpha

## Conclusion
All the models have comparable scores varying only slightly. All have a high accuracy score for the both the train and test data.  Therefore, there is both low variance and low bias. There some outliers which tell that the model is not scoring as well on a few high price homes so there is still room to improve. With more time and resources I would want to improve my models further.

As also, to better deal with ordinal features with better encoding schemes. Relying on discrete values for ordinal variables is very preliminary and really don't reflect the actual conditions.

The model, however, may have limited applicability because it was constructed using data from houses sold in Ames, Iowa between 2006 and 2010. The scope of this dataset is limited, both in terms of time frame and geographic range. The four-year time range is insufficient to capture any annual price variations that may occur as a result of external factors such as the present economy. Inflation may have influenced housing prices in the current year (2019). The model is also specific to Ames homes and may not be as accurate when applied to data from another city or nation, where house prices are influenced by factors other than garage quality, for example.

Any mathematical model can not really capture behavioral aspects. So, however much we tune it, there will always be an uncertain aspect. So, this entire exercise can only be indicative.
