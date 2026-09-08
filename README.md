# Practical Labs 5
# Classification

## Setup

Before performing the task, you need to set up the development environment.

### Creating a Python virtual environment

1. For Windows:
    ```powershell
    python -m venv venv
    ```

2. For Linux/macOS:
    ```bash
    python3 -m venv venv
    ```

### Activating the virtual environment

1. For Windows:
    ```powershell
    .\venv\Scripts\activate
    ```

2. For Linux/macOS:
    ```bash
    source venv/bin/activate
    ```

> [!NOTE]
> After activating the virtual environment, you will see the `(venv)` prefix in front of the command line.

### Installing the required packages from the `requirements.txt` file

1. For both systems:
    ```bash
    pip install -r requirements.txt
    ```

## Task 1. Binary Classification Using Logistic Regression

#### Problem Description
You are tasked with implementing **Logistic Regression** for a binary classification problem. Your solution should:
1. Read a dataset (`data.csv`) containing two features (`Feature1` and `Feature2`) and a target (`Target` with values 0 or 1).
2. Train a **Logistic Regression** model to classify the target variable based on the two features.
3. Evaluate the model using metrics:
   - **Accuracy**
   - **Precision**
   - **Recall**
   - **F1-Score**
4. Visualize the data and the decision boundary using **Matplotlib**.

### Sample Data
```
Feature1,Feature2,Target
2.5,1.8,1
1.2,0.9,0
3.1,2.4,1
0.8,1.2,0
2.9,2.1,1
```

### File Structure
```
project/
├── data.csv
└── src/
    └── logistic_regression.py
```

### Methods Description
- `read_csv(file_path)`: Reads CSV file and returns pandas DataFrame
- `train_logistic_regression(X, y)`: Trains logistic regression model using scikit-learn
- `evaluate_model(y_true, y_pred)`: Calculates accuracy, precision, recall, and F1-score
- `visualize_decision_boundary(X, y, model)`: Creates scatter plot with decision boundary

### Expected Output
- Script Output:
  - Evaluation metrics: Accuracy, Precision, Recall, F1-Score.
  - Visualization of the decision boundary.


## Task 2. Classifying Data Using Decision Trees

#### Problem Description
You are tasked with building a **Decision Tree Classifier** to classify data into two categories. Your solution should:
1. Read a dataset (`data.csv`) containing two features (`Feature1` and `Feature2`) and a target (`Target` with values 0 or 1).
2. Train a **Decision Tree Classifier** on the dataset.
3. Evaluate the classifier using metrics:
   - **Accuracy**
   - **Precision**
   - **Recall**
   - **F1-Score**
4. Visualize the decision boundaries of the Decision Tree model using **Matplotlib**.

### Sample Data
```
Feature1,Feature2,Target
1.5,2.0,1
0.8,1.2,0
2.2,1.8,1
1.0,0.5,0
2.8,2.5,1
```

### File Structure
```
project/
├── data.csv
└── src/
    └── decision_tree.py
```

### Methods Description
- `read_csv(file_path)`: Reads CSV file and returns pandas DataFrame
- `train_decision_tree(X, y, max_depth)`: Trains decision tree classifier with optional max_depth parameter
- `evaluate_model(y_true, y_pred)`: Calculates accuracy, precision, recall, and F1-score
- `visualize_decision_boundary(X, y, model)`: Creates scatter plot with decision tree boundaries

### Expected Output
- **Script Output**: Evaluation metrics and a decision boundary visualization.


## Task 3. Classifying Data Using K-Nearest Neighbors (K-NN)

#### Problem Description
You are tasked with implementing a **K-Nearest Neighbors (K-NN)** classifier to predict binary class labels based on two features. Your solution should:
1. Read a dataset (`data.csv`) containing two features (`Feature1` and `Feature2`) and a target (`Target` with values 0 or 1).
2. Train a **K-NN Classifier** on the dataset.
3. Evaluate the classifier using metrics:
   - **Accuracy**
   - **Precision**
   - **Recall**
   - **F1-Score**
4. Visualize the decision boundaries using **Matplotlib**.

### Sample Data
```
Feature1,Feature2,Target
1.2,2.1,1
0.9,1.5,0
2.3,2.8,1
1.5,0.8,0
2.7,2.2,1
```

### File Structure
```
project/
├── knn_classifier.csv
└── src/
    └── knn_classifier.py
```

### Methods Description
- `read_csv(file_path)`: Reads CSV file and returns pandas DataFrame
- `train_knn_classifier(X, y, k)`: Trains K-NN classifier with specified number of neighbors (k)
- `evaluate_model(y_true, y_pred)`: Calculates accuracy, precision, recall, and F1-score
- `visualize_decision_boundary(X, y, model)`: Creates scatter plot with K-NN decision boundaries

### Expected Output
- **Script Output**:
  - Evaluation metrics: Accuracy, Precision, Recall, F1-Score.
  - Visualization of the decision boundary.
