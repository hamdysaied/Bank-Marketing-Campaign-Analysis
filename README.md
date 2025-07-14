# Bank Marketing Campaign Analysis

### Dataset Overview

The dataset contains information about bank marketing campaigns with the following key features:

**Demographic Information:**
- `age`: Customer age
- `job`: Type of job (blue-collar, management, technician, etc.)
- `marital`: Marital status
- `education`: Education level

**Campaign Details:**
- `contact`: Contact communication type (cellular, telephone)
- `month`: Last contact month
- `day_of_week`: Last contact day of the week
- `duration`: Last contact duration in seconds
- `campaign`: Number of contacts performed during this campaign
- `pdays`: Number of days since last contact from previous campaign
- `previous`: Number of contacts performed before this campaign
- `poutcome`: Outcome of previous marketing campaign

**Target Variable:**
- `y`: Has the client subscribed to a term deposit? (yes/no)

### Project Structure

```
├── DataToolsProject-final.ipynb    # Main analysis notebook
├── README.md                       # This file
└── data/                          # Dataset files (if applicable)
```

### Key Features

#### Data Preprocessing
- **Missing Value Handling**: Conversion of "unknown" values to NaN for proper treatment
- **Feature Engineering**: Creation of `duration_min` feature (duration in minutes)
- **Encoding**: 
  - Label encoding for binary categorical variables
  - One-hot encoding for multi-category variables
- **Data Balancing**: SMOTE (Synthetic Minority Oversampling Technique) implementation

#### Feature Selection Techniques
- **Variance Threshold**: Removes low-variance features
- **SelectKBest**: Statistical feature selection using f_classif
- **SelectFromModel**: Model-based feature selection
- **Recursive Feature Elimination (RFE)**: Iterative feature selection

#### Machine Learning Models
- **Decision Tree Classifier**
- **Random Forest Classifier**
- **Logistic Regression**
- **K-Nearest Neighbors (KNN)**
- **Neural Networks** (TensorFlow implementation)

### Dependencies

```python
pandas
numpy
matplotlib
seaborn
scikit-learn
category_encoders
tensorflow
imbalanced-learn
```

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/bank-marketing-analysis.git
cd bank-marketing-analysis
```

2. Install required packages:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn category_encoders tensorflow imbalanced-learn
```

3. Run the Jupyter notebook:
```bash
jupyter notebook DataToolsProject-final.ipynb
```

### Usage

The notebook follows a structured approach:

1. **Data Loading and Exploration**: Initial data inspection and statistical analysis
2. **Data Preprocessing**: Cleaning, encoding, and feature engineering
3. **Feature Selection**: Multiple techniques for optimal feature subset selection
4. **Model Training**: Implementation of various classification algorithms
5. **Model Evaluation**: Performance comparison using accuracy, classification reports, and confusion matrices

### Key Insights

- Dataset contains **32,941 records** with mixed data types
- Target variable shows class imbalance (addressed with SMOTE)
- Duration of contact appears to be a significant predictor
- Multiple feature selection techniques help identify most relevant variables

### Model Performance

The notebook implements comprehensive model evaluation including:
- Accuracy scores
- Classification reports (precision, recall, F1-score)
- Confusion matrices
- Cross-validation results

### Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request


