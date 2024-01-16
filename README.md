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

### Steps
  1. Data Collection
     - source: [https://lvr.land.moi.gov.tw/](https://lvr.land.moi.gov.tw/)
     - Retrieve the housing information API of the mentioned webpage using F12, and use the 'requests' library to fetch the content.
  2. Handling missing values
  3. Label Encoding
  4. One Hot Encoding
  5. Sub-features Separation
  6. remove outliers
  7. Normalization
  
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
  4. Training
  5. Visialize training result and pick new param manually(i.e. go to step3) for hyper param training 
  6. Retrain and testing
  7. Visialize retrain and testing
## Random forest
## NN

###  Installation
  - tensorflow 
  - numpy
  - pandas
  - matplotlib
  - sklearn

<img width="350" alt="training" src="https://github.com/k38670462/ML_Project/assets/41421967/b0eb9c62-7cb7-4480-bf07-0a71cd8ecf5e">
  
-

<img width="344" alt="predction" src="https://github.com/k38670462/ML_Project/assets/41421967/c0a0f323-00ac-4df9-bf96-418dc759493a">
