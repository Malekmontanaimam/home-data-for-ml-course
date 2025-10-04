# House Price Prediction Project

## Project Overview

This project is an advanced machine learning model for predicting house prices in Ames, Iowa, USA. The model was developed using various machine learning techniques to achieve the best possible accuracy in real estate price prediction.

## Project Goals

The main objectives of this project are:

1. **Develop an accurate machine learning model** to predict house prices based on their various characteristics
2. **Compare the performance of different algorithms** in machine learning to select the best one
3. **Improve prediction accuracy** through feature engineering
4. **Apply best practices** in data processing and model evaluation

## Data Used

### Data Sources:
- **train.csv**: Training data (1460 houses) with their actual prices
- **test.csv**: Test data (1459 houses) for price prediction
- **data_description.txt**: Detailed description of all variables in the data

### Data Characteristics:
- **79 different variables** describing house characteristics
- **Numerical variables**: such as lot area, year built, number of rooms
- **Categorical variables**: such as neighborhood type, heating type, kitchen quality

## Approach

### 1. Data Processing
- **Handling missing values**: Using median for numerical values and "Unknown" for categorical
- **Categorical variable encoding**: Using Label Encoding
- **Feature engineering**: Creating new variables such as:
  - `TotalSF`: Total square footage
  - `TotalBath`: Total number of bathrooms
  - `Age`: House age
  - `HasPool`, `HasFireplace`, `HasGarage`: Indicators for specific features

### 2. Models Used
Four different models were tested:

1. **Random Forest Regressor**
   - Number of trees: 400
   - Maximum depth: 20

2. **Gradient Boosting Regressor** ⭐ (Best)
   - Number of trees: 400
   - Maximum depth: 6
   - Learning rate: 0.05

3. **HistGradientBoosting Regressor**
   - Maximum depth: 8
   - Learning rate: 0.05

4. **Linear Regression**

### 3. Model Evaluation
- **Evaluation metric**: Mean Absolute Error (MAE)
- **Cross-validation**: 5-Fold Cross Validation
- **Data split**: 80% training, 20% validation

## Results Achieved

### Model Performance:
| Model                 |     MAE    |
|-----------------------|------------|
| Random Forest         |  16,689    |
| **Gradient Boosting** | **15,408** |
| HistGradientBoosting  |   15,800   |
| Linear Regression     |   15,762   |

### Best Model:
- **Gradient Boosting Regressor** achieved the best performance
- **MAE**: $15,408
- **Cross-Validation MAE**: $16,103 ± $1,301

### Most Important Features:
1. **OverallQual** (Overall Quality): 45.2%
2. **TotalSF** (Total Square Footage): 29.4%
3. **CentralAir** (Central Air Conditioning): 2.2%
4. **GrLivArea** (Living Area): 2.1%
5. **GarageArea** (Garage Area): 1.7%

## Important Files

- `improved_model.ipynb`: Main Jupyter notebook containing the complete code
- `improved_submission.csv`: Final predictions file for testing
- `train.csv`: Training data
- `test.csv`: Test data
- `data_description.txt`: Detailed description of variables

## Technologies Used

### Python Libraries:
- **pandas**: Data processing
- **numpy**: Mathematical operations
- **scikit-learn**: Machine learning algorithms
- **matplotlib/seaborn**: Visualization (if used)

### Machine Learning Algorithms:
- Random Forest
- Gradient Boosting
- Histogram-based Gradient Boosting
- Linear Regression

## Lessons Learned

1. **Feature engineering is very important**: Creating new variables like TotalSF and Age significantly improved performance
2. **Overall house quality** is the most influential factor in price
3. **Gradient Boosting** showed excellent performance with this data
4. **Proper handling of missing values** is essential for accurate results

**Note**: This project is part of the House Prices competition on Kaggle and aims to apply machine learning concepts in the real estate field.
