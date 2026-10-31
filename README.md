# Smoking Status Prediction       
   
A machine learning project that predicts smoking status based on various health and demographic indicators using classification algorithms.

## 📋 Project Overview

This project builds and optimizes machine learning models to predict whether an individual is a smoker or non-smoker based on health metrics and demographic data. The analysis includes data preprocessing, exploratory data analysis (EDA), model training, hyperparameter tuning, and performance evaluation.

## 📁 Project Structure

```
smoking-status-prediction/
├── Smoking.ipynb                 # Main Jupyter notebook with complete analysis
├── smoking.csv                   # Original dataset
├── x_train.csv                   # Training features
├── x_test.csv                    # Testing features
├── y_train.csv                   # Training target labels
├── y_test.csv                    # Testing target labels
└── README.md                      # This file
```

## 🔍 Dataset

The dataset contains health and lifestyle information used to predict smoking status:

- **Features**: Gender, age-related metrics, and oral health indicators (tartar, cavities)
- **Target Variable**: Smoking status (binary classification)
- **Data Format**: CSV files with preprocessed train/test split

### Key Features:
- `gender`: Patient gender (M/F)
- `oral`: Presence of oral health issues (Y/N)
- `tartar`: Tartar buildup presence (Y/N)
- Various numerical health metrics

## 🛠️ Data Preprocessing

The notebook performs comprehensive data preparation:

1. **Data Loading**: Imports datasets and performs initial data inspection
2. **Exploratory Data Analysis**: 
   - Examines data types and structure
   - Checks for missing values and duplicates
   - Generates descriptive statistics
3. **Encoding**: Converts categorical variables (gender, oral, tartar) to numerical format
4. **Outlier Detection & Treatment**: 
   - Uses IQR (Interquartile Range) method to identify outliers
   - Caps extreme values at the bounds
5. **Feature-Target Separation**: Splits data into features (X) and target (y)

## 🤖 Models & Algorithms

### 1. Logistic Regression
- Basic baseline model for binary classification

### 2. Decision Tree Classifier
Multiple implementations with varying hyperparameters:

- **Basic Model**: Default DecisionTreeClassifier
- **Tuned Models**: Various configurations with different:
  - `criterion`: gini or entropy
  - `max_depth`: 2, 4, 6, 8, 10, 12
  - `min_samples_split`: 10, 20, 30, ..., 100

### 3. Grid Search Optimization
Automated hyperparameter tuning using GridSearchCV to find the best parameter combination

## 📊 Evaluation Metrics

The models are evaluated using:

- **Accuracy Score**: Overall correctness on training and test sets
- **Classification Report**: 
  - Precision
  - Recall
  - F1-Score
  - Support

## 🚀 Key Workflow Steps

1. **Data Preparation**: Load and clean the data
2. **Exploratory Analysis**: Understand data distributions and relationships
3. **Feature Engineering**: Encode categorical variables
4. **Outlier Handling**: Apply IQR-based capping
5. **Model Selection**: Train multiple classification models
6. **Hyperparameter Tuning**: Use GridSearchCV for optimization
7. **Model Evaluation**: Compare train/test performance
8. **Visualization**: Generate decision tree rules and diagrams

## 🎯 Results & Insights

The analysis includes:
- Train vs. Test accuracy scores for each model configuration
- Decision tree visualizations showing decision rules
- Classification metrics for detailed performance analysis
- Optimal hyperparameter identification

## 💻 Requirements

- pandas
- numpy
- matplotlib
- scikit-learn

## 📝 Usage

1. Open `Smoking.ipynb` in Jupyter Notebook or JupyterLab
2. Ensure all CSV files are in the same directory
3. Run cells sequentially to execute the analysis
4. Visualizations and performance metrics will be displayed

## 🔧 Customization

You can modify:
- Hyperparameter ranges in GridSearchCV
- Train/test split ratio
- Outlier detection sensitivity (IQR multiplier)
- Model selection criteria

## 📈 Next Steps for Enhancement

- Experiment with ensemble methods (Random Forest, Gradient Boosting)
- Perform feature importance analysis
- Cross-validation implementation
- Class balancing techniques (if imbalanced)
- Feature scaling/normalization for comparison

## 📄 License

This project is provided as-is for educational and analysis purposes.
