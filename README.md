# Safeguarding Shores: A Categorical Model for Flood Prediction from Historical Water Levels

## Project Description

According to the World Health Organisation (WHO), floods are the most common type of natural disaster, occurring when water overflows and submerges typically dry areas. In Malaysia, multiple waves of floods occur at the end of every year, posing a serious threat to residents, homes, and infrastructure.

This project aims to address the rising frequency of floods in Sungai Pahang, Malaysia, by developing advanced flood prediction and mitigation technologies, with a particular emphasis on Kelantan, Terengganu, and Sungai Pahang. Using machine-learning algorithms such as decision trees and SVMs, along with data collected from meteorological and environmental factors, this study will develop a machine-learning model capable of predicting different types of floods.

## Objectives

1. To reduce the damage caused by floods to human communities, ecosystems, and wildlife.
2. To develop a machine learning model to predict whether a flood is likely to occur.
3. To evaluate the performance of the model using:
   - Decision Tree
   - Support Vector Machines (SVM)
   - Random Forest
   - Gradient Boosting
   - XGBoost

## Data Description

The dataset includes daily measurements of various environmental factors, such as:
- Rainfall
- Water level
- Streamflow
- Weather conditions

![image](https://github.com/user-attachments/assets/7a0adaac-d6ad-43aa-9c46-d0a13d9e7f0a)

## Data Preprocessing

### Data Preparation
- **Datasets**: Eight datasets (rainfall, water level, streamflow, and weather) from 2021 and 2022.
- **Reshaping Data**: The `Day` column was used as the identifying variable, and the `melt` function was applied to convert datasets into long format.
- **Combining Data**: Data for 2021 and 2022 for each variable was combined, merging the four datasets into a single dataset.

### Handling Missing Data
- Missing values in the `Weather` column were removed.
- Missing values in the `WaterLevel` column (days 40 to 60) were filled using linear interpolation.
- Unknown data indicated by question marks (`?`) were replaced with NaN, and missing rainfall data was filled with zeros.

### Classification Thresholds
- A new column, `Threshold`, was added to classify water levels as:
  - Normal
  - Alert
  - Warning
  - Danger

### Correlation Analysis
- A correlation heatmap revealed:
  - Slightly strong correlation between water level and streamflow (0.42).
  - Weak correlation between water level and rainfall (0.14).
  - Slightly strong negative correlation between weather and water level (-0.41).
 
![image](https://github.com/user-attachments/assets/0d357459-8dcd-4782-8c50-bd12b7ca3271)


## Model Development

### Assigning Target and Features
- The target variable (`Threshold`) and features (rainfall, water level, streamflow, and weather) were identified for model training.

### Data Partitioning
- The dataset was partitioned into training and testing subsets.

### Balancing the Dataset
- Techniques were applied to address dataset imbalance to ensure accurate model training and evaluation.

## Results

Model performance will be evaluated using accuracy, precision, recall, and F1-score to compare the effectiveness of different algorithms.

## More Details
You can also go to Medium for a more detailed explanation of this project, using the link [Water Level Prediction and Flood Alert Based on Historical Data].

[Water Level Prediction and Flood Alert Based on Historical Data]: https://medium.com/@limbingsern123/water-level-prediction-and-flood-alert-based-on-historical-data-24508aa9cac2
