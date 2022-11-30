# data606_venkata

Here is the dataset download link: https://opendata.maryland.gov/widgets/65du-s3qu
 
Youtube video link : https://www.youtube.com/watch?v=b4bxoAH7F5o

# Maryland Statewide Vehicle Crashes
## Name: Venkata Satya Praneeth
![image](https://user-images.githubusercontent.com/103671539/204929641-d146ff16-9b72-46be-be28-5421a1a36345.png)
## INTRODUCTION
- This is the public dataset from the Maryland open information source(https://opendata.maryland.gov/). I utilized Jupyter note pad and python language to code. The dataset addresses the vehicle crashes across the Maryland state. This dataset has 8,22,412 rows and 56 columns. These features include the time, place, cause, climate, street type and so forth connected with the mishaps. The dataset is downloaded in CSV format and utilized for the project. The dataset is cleaned by taking care of invalid qualities, missing qualities, and any ill-advised information.

## ABSTRACT
- I chose "REPORT TYPE" as my target column. There are three classes are represented in the target variable: "Property Damage Crash," "Injury Crash," and "Fatal Crash." To minimize a conflict with multiple classes, those three classes are reduced into two by altering Fatal Crash into Injury Crash. This is likewise done for the alternative explanation that Fatal Crash corresponds to accidents that result in death, being a subclass of an Injury crash. As more than just a result, the final target variable only has two classes.
  
## DATASET INSIGHTS
The dataset is considered from Maryland open information. 
- Only the columns "MUNI DESC," "RTE SUFFIX," and "REFERENCE SUFFIX" have null values, and the column "AREA CODE" has unknown values. So, these columns are removed.
- There are several categories that numerically correspond identically to other columns. Furthermore, the dataset removes those columns. We are unable to comprehend anything or make any conclusions from some of those numerical columns individually.
- I used WEATHER_DESC, COUNTY_DESC, LIGHT_DESC, COLLISION_TYPE_DESC, LOCATION in analysis

## DATASET LINK
Here is the Dataset link https://opendata.maryland.gov/widgets/65du-s3qu
There are 56 columns and 8,22,412 rows in the dataset. 

## COLUMNS DESCRIPTION 

YEAR - Values are from 2016 - 2021

QUARTER - Values of four quarters Q1 to Q4

LIGHT_DESC - Description of light of the day like Daylight, dark, dark no lights, etc.

LIGHT_CODE - Numerical representation of LIGHT_DESC column.

COUNTY_DESC - Counties list like Baltimore, Baltimore city, etc.

COUNTY_NO - Numerical representation of COUNTY_DESC column.

MUNI_DESC - This column is ambigous, it contains only null values and not clear about this column.

MUNI_CODE - Numerical representation of MUNI_DESC column.

JUNCTION_DESC - Describes the type of junction at the time of crash like Two-way junction, etc.

JUNCTION_CODE - Numerical representation of JUNCTION_DESC column.

COLLISION_TYPE_DESC- Describes how collision occured.

COLLISION_TYPE_CODE- Numerical representation of COLLISION_TYPE_DESC column.

SURF_COND_DESC - Describes the surface condition of the road at the time of accident like Dry, wet, etc.

SURF_COND_CODE - Numerical representation of SURF_COND_DESC column.

LANE_DESC - Describes the type of lane like left lane, right lane, etc.

LANE_CODE - Numerical representation of LANE_DESC column.

RD_COND_DESC - Describes the condition of road like it contains any defects or no defects.

RD_COND_CODE - Numerical representation of RD_COND_DESC column.

RD_DIV_DESC - Describes how the road is divided like one way, two-way, etc.

RD_DIV_CODE - Numerical representation of RD_DIV_DESC column.

FIX_OBJ_DESC - Describes the property near the accident or the property that damaged due to the accident.

FIX_OBJ_CODE - Numerical representation of FIX_OBJ_DESC column.

REPORT_NO - It is the unique number, it represents file of each accident.

REPORT_TYPE - Represents the type of accident like property damage or injury crash or fatal crash.

WEATHER_DESC - Describes the weather condition.

WEATHER_CODE - Numerical representation of WEATHER_DESC column.

ACC_DATE - Accident date

ACC_TIME - Accident time

LOC_CODE - Location code represents each county

SIGNAL_FLAG_DESC - Direction flag like north, west, east, south.

SIGNAL_FLAG - Shortforms of SIGNAL_FLAG_DESC.

C_M_ZONE_FLAG - Contains two values N and Y.

AGENCY_CODE - Agency code of counties.

AREA_CODE - Area code of counties.

HARM_EVENT_DESC1 - Describing cause of accident.

HARM_EVENT_CODE1 - Numerical representation of HARM_EVENT_DESC1 column.

HARM_EVENT_DESC2 - Describing cause of accident.

HARM_EVENT_CODE2 - Numerical representation of HARM_EVENT_DESC2 column.

RTE_NO - Route number.

ROUTE_TYPE_CODE - Short form counties.

RTE_SUFFIX - No description for this column, it contains null values.

LOG_MILE - Distance from the accident to nearby survey zone.

LOGMILE_DIR_FLAG_DESC - Direction of which accident occured.

LOGMILE_DIR_FLAG - Short form of LOGMILE_DIR_FLAG_DESC.

MAINROAD_NAME - Mainroad name at which accident occurred.

DISTANCE - Distance.

FEET_MILES_FLAG_DESC - Feet or miles flags description

FEET_MILES_FLAG - Shortforms of FEET_MILES_FLAG_DESC

DISTANCE_DIR_FLAG - Distance direction flags like N,S, W, E.

REFERENCE_NO - Reference number.

REFERENCE_TYPE_CODE - Reference number type code.

REFERENCE_SUFFIX - It is a null values column.

REFERENCE_ROAD_NAME - Reference road name to locate the point of accident.

LATITUDE - Latitude points.

LONGITUDE - Longitude points.

LOCATION - combination of latitude and longitude points.

## ML MODELS
These are the Machine Learning Models I Implemented:
1.	Logistic regression
2.	 Random Forest
3.	 Decision Tree

Depending on the type of classification, clustering, and regression, I would like to create various statistics and visualizations, such as accuracy, confusion matrix and ROC curve. I chose the model that best fits the data according to its performance, recall, and accuracy.

## Results and Conclusion

Started with Modeling with three classification algorithms. Logistic regression, Random Forest, Decision Tree. While modeling GridSearchCv is used to find the best parameters of the algorithms. After getting best parameters from the GridSearchCv. If the parameters are changed then those best parameters are used to predict the target variable on the test data. Classification report, accuracy score  is visualized. Roc_auc curve is plotted and area under roc_auc curve is calculated. Using all the results the model performance is compared with other models. The same steps are repeated for all the algorithms.\


Finally, got the accuracy of all algorithms. we can observe Logistic regression is performed best among remaining algorithms. Random Forest algorithm is performed least.\ 
The accuracy of the Decision Tree algorithm is about 73%.
The accuracy of the logistic regression algorithm is about 73%.
The accuracy of the random forest algorithm is about 60%. \
After analyzing the three models, I think Logistic Regression Classifier has ROC_AUC score is 70% can classify better compared to others. We can improve the accuracy by dealing the dataset imbalance through better modeling techniques.

These predictions can help insurance agencies to work on respective cases based on type of accidents.


 
## REFRENCES:
Maryland Statewide Vehicle Crashes | Open Data | [opendata.maryland.gov](url)
