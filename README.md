# Crime Statistics Classification Analysis
A comparative study of machine learning classification methods applied to crime statistics data.

## Contributing
This is a group project for *Predictive Modeling Analytics* . Contributors:
- Dimas Gistha Adnyana - Data preprocessing and k-NN implementation
- Nada Putri Pambudi - Naïve Bayes and Logistic Regression
- Ameera Maritza Zayda - SVM and Decision Tree
- Aqila Aulia - BPNN implementation

#PLACEHOLDER README

## Project Overview
This project implements and compares multiple classification algorithms to predict crime categories using a comprehensive crime statistics dataset. The analysis includes implementations of:
- k-Nearest Neighbors (k-NN)
- Naïve Bayes
- Logistic Regression
- Support Vector Machines (SVM)
- Decision Trees
- Back Propagation Neural Networks (BPNN)

## Repository Structure
```
├── data/
│   ├── raw/                # Original crime statistics dataset
│   └── processed/          # Preprocessed and split datasets
├── notebooks/
│   ├── 1_data_splitting.ipynb     # Data preparation and splitting
│   ├── 2_knn_classification.ipynb  # k-NN implementation
│   ├── 3_naive_bayes.ipynb        # Naïve Bayes implementation
│   ├── 4_logistic_regression.ipynb # Logistic Regression
│   ├── 5_svm_classification.ipynb  # SVM implementation
│   ├── 6_decision_tree.ipynb      # Decision Tree implementation
│   └── 7_bpnn_classification.ipynb # BPNN implementation
├── src/
│   ├── data/              # Data processing scripts
│   ├── features/          # Feature engineering scripts
│   └── models/            # Model implementation scripts
├── results/               # Performance metrics and analysis
└── requirements.txt       # Project dependencies
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/your-username/crime-statistics-classification.git
cd crime-statistics-classification
```

2. Create and activate a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

## Data Preprocessing
The preprocessing pipeline includes:
- Data splitting (70% training, 30% test)
- Feature standardization
- Stratified sampling
- 5-fold cross-validation setup

## Model Implementation
Each classification method is implemented with the following considerations:

### k-NN Classification
- Multiple k values testing
- Cross-validation performance evaluation
- Metric calculations (accuracy, precision, recall, F1-score, AUC ROC)

### Naïve Bayes
- 5-fold cross-validation
- Performance metrics evaluation
- Model optimization

### Logistic Regression
- Standard implementation
- Cross-validation results
- Performance analysis

### SVM
- Linear and RBF kernel implementations
- C parameter optimization
- Cross-validation evaluation

### Decision Tree
- Multiple parameter combinations testing
- Depth and split criteria optimization
- Performance evaluation

### BPNN
- Hidden layer configuration testing
- Learning rate optimization
- Activation function comparison

## Usage
1. Data Preparation:
```python
from src.data import prepare_data
X_train, X_test, y_train, y_test, cv = prepare_data()
```

2. Model Training:
```python
# Example for k-NN
from src.models import train_knn
model, metrics = train_knn(X_train, y_train, cv)
```

3. Evaluation:
```python
from src.models import evaluate_model
results = evaluate_model(model, X_test, y_test)
```

