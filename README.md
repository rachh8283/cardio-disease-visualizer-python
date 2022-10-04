# cardio-disease-visualizer-python
Visualize and make calculations from medical exam data using seaborn, matplotlib, pandas, and numpy. 

## Data set 
This data set includes information about patients including body measurements, lab results for certain tests, and lifestyle. 

## Goal
Explore the relationship between cardiovascular disease, lifestyle choices, body measurements, and blood test results. 
Create a chart that shows counts for good and bad outcomes for cholesterol, glucose, alcohol, active, and smoking variables in patinets with cardiovascular disease (cardio=1) and without disease (cardio=0).

## Tasks
-  Add obese column by calculating BMI that is over 30. Calculated by dividing weight in kg by height in m. If the value is > 30, the person is obese, using 0 for not obese and 1 for obese. 
-  Data normalized so 0 is always good and 1 is always bad.
-  Changed  values for cholesterol and glucose to 0 if = 1 or 1 if greater than 1. 
-  Converted data to long format and created a chart for counts of above categorical features using catplot(). Data set split by "cardio" with chart for each value. 
-  Clean data to filter out patient segments with incorrect data including:
    -  diastolic pressure is higher than systolic (Keep the correct data with (df['ap_lo'] <= df['ap_hi']))
    -  height is less than the 2.5th percentile (Keep the correct data with (df['height'] >= df['height'].quantile(0.025)))
    -  height is more than the 97.5th percentile
    -  weight is less than the 2.5th percentile
    -  weight is more than the 97.5th percentile
 - Created correlation matrix and plotted it in heatmap, masking upper triangle. 

## Interpretation
This data indicates that most of the variables are strongly correlated with heart disease. In the catplot bar chart, cholesterol and obesity are most dramatic The heat map shows the most correlated variables to be weight-obesity, gender-smoke, cholesterol-glucose, and gender-height.
