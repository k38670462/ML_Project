# House Price Prediction Model

This project focuses on comparing different machine learning models for predicting house prices. Python is used for the implementation, and various libraries are employed for data analysis, visualization, and machine learning.

## Data preprocessing

###  Libraries
  - pandas
  - requests
  - numpy
  - cn2an
  - seaborn
  - sklearn

### Introduction
- Data Collection
: Retrieve the housing information API of the mentioned webpage using F12, and use the 'requests' library to fetch the content.
  - source: [https://lvr.land.moi.gov.tw/](https://lvr.land.moi.gov.tw/)
    
- Handling missing values
: If directly deleting rows with missing values, it would significantly reduce the dataset. Therefore, I have filled in the missing values with the mode of the respective column.
    
- Label Encoding
: Convert the information about 'elevator' and 'janitor' (whether they are present or not) into numerical values using the label encoding method.
    
- One Hot Encoding
: After simplifying complex information such as 'property' and 'floor' through some basic processing, transform them into numerical values using one-hot     encoding.

- Sub-features Separation
: Split the 'layout' information into separate columns for bedroom, living room, and bathroom.
    
- Remove outliers
: We improved the dataset quality by identifying and eliminating outliers, as they can distort results and impact the model's performance, ensuring more accurate and reliable predictions.
    
- Normalization
: We performed min-max normalization on the data to standardize all numeric features to a common scale, preserving differences in value ranges. This normalization is crucial for models sensitive to data scale, significantly impacting performance."

  
## XGBoost
  use conda to install xgboost please refer https://anaconda.org/conda-forge/xgboost
  
  ```
  conda install conda-forge::xgboost
  ```
  
  ###  Installation
  - xgboost
  - numpy
  - pandas
  - matplotlib

### Steps
  1. Import packet
  2. Input data and init
  3. Params setting
     
    
    #starting param
    params = {'learning_rate': 0.1,  'max_depth': 5, 'min_child_weight': 1, 'seed': 0,
                    'subsample': 0.8, 'colsample_bytree': 0.8, 'gamma': 0, 'reg_alpha': 0, 'reg_lambda': 1}
    
    #pick pram by by following order
    #minchildweight[i for i in range(10)] and max_depth[i for i in range(10)]
    #gamma[0,inf]
    #subsample(0.5,1] and colsample_bytree(0,1]
    #regalpha[0,inf] and reglambda[0,inf]
    #learning_rate (0,inf]
  5. Training
  6. Visialize training result and pick the best param one by one manually by using checkpointing (i.e. go to step3) for hyper param training 
  7. Retrain and testing
  8. Visialize retrain and testing

  ### Final Result

  <img width="350" alt="result" src="https://github.com/k38670462/ML_Project/blob/main/xgb/final_result.png">

## Random forest

### Overview
This part focuses on predicting house prices using Random Forest Regressor algorithm. The dataset used for training and testing contains information about various features related to houses.

### Running the Code
- Make sure to install all required **libraries**.
- Adjust **file paths** for the training and testing datasets according to your file paths.
- Run the script to train the Random Forest Regressor and then visualize the results.

### Project Structure
1. **Data Loading and Preprocessing:** Data preprocessing includes converting data types, handling missing values, and slicing features and labels for training.
2. **Random Forest Regressor Model:** The Random Forest Regressor is employed for predicting house prices. The model is configured with default parameters and later fine-tuned using a grid search to optimize its performance.
3. **Hyperparameter Tuning:** By using grid search cross validation, the goal is to find the best combination of hyperparameters which maximizes the R2 score.
4. **Results Visualization:** This part includes visualizations to demonstrate the impact of different hyperparameters on the R2 score and training times. It also displays feature importances to understand which features contribute most to the predictions.

### Code Structure
- The DataPreprocessing function handles loading, converting data types, and imputing missing values.
- The RandomForest function initializes and fits the Random Forest Regressor.
- The AutoTuningGrid function performs hyperparameter tuning using grid search and cross-validation.
- Other functions `ShowCVResults`, `ShowR2`, ShowFeatureImportances generate visualizations to understand the model's performance and feature importance.

### Results
- The implementation of random forest provides R2 scores for training and testing datasets, illustrating the model's accuracy.
- Hyperparameter tuning results are displayed as well, showing the impact of different parameters on R2 scores and training times.
- Feature importances are visualized to highlight the most influential features in predicting house prices.

Feel free to modify the code to suit your specific dataset and requirements.

## NN

###  Installation
  - tensorflow 
  - numpy
  - pandas
  - matplotlib
  - sklearn
### Steps
  1. Import packet
  2. Input the data
  3. Create model and setting hyperparameters
  4. Training
  5. Visialize training result

<div align="center">
    <a href="./">
        <img src="https://github.com/k38670462/ML_Project/assets/41421967/b0eb9c62-7cb7-4480-bf07-0a71cd8ecf5e" width="80%"/>
    </a>
</div>
-
<div align="center">
    <a href="./">
        <img src="https://github.com/k38670462/ML_Project/assets/41421967/c0a0f323-00ac-4df9-bf96-418dc759493a" width="80%"/>
    </a>
</div>
