# Decision Tree Regression – House Price Prediction

## Project Overview

This project implements a Decision Tree Regression model to predict house prices using property features. It also explores fundamental Decision Tree concepts, including Entropy, Information Gain, Gini Impurity, Pre-Pruning, Post-Pruning, and Hyperparameter Tuning.

The project demonstrates how Decision Trees make predictions, how splitting criteria work, and how model performance can be improved through cross-validation and hyperparameter optimization.

## Dataset

**Dataset:** House Prices Dataset

The dataset contains 10,000 records with four input features and one target variable.

| Feature | Description |
|---|---|
| `square_feet` | Area of the house |
| `num_rooms` | Number of rooms |
| `age` | Age of the house |
| `distance_to_city(km)` | Distance from the city |
| `price` | Target variable – House price |

## Technologies Used

- Python
- Pandas and NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- Visual Studio Code
- Git and GitHub Desktop

## Concepts Implemented

1. **Decision Tree Regression:** Trained and visualized a Decision Tree Regressor using squared error.
2. **Information Gain:** Calculated entropy-based Information Gain using a classification example and squared error reduction using the regression dataset.
3. **Entropy:** Calculated and visualized entropy for different binary class distributions.
4. **Pre-Pruning:** Controlled tree growth using `max_depth`, `min_samples_split`, and `min_samples_leaf`.
5. **Post-Pruning:** Implemented cost-complexity pruning using `ccp_alpha`.
6. **Gini Impurity and Gini Index:** Calculated and visualized Gini impurity using binary classification examples.
7. **Hyperparameter Tuning:** Applied GridSearchCV with five-fold cross-validation to optimize Decision Tree parameters.

## Machine Learning Workflow

1. Loaded the dataset and performed Exploratory Data Analysis (EDA).
2. Examined missing values, duplicates, distributions, and feature correlations.
3. Split the dataset into 80% training and 20% testing data.
4. Trained an initial Decision Tree Regressor.
5. Evaluated performance using MAE, MSE, RMSE, and R².
6. Explored Pre-Pruning and Post-Pruning.
7. Performed hyperparameter tuning using GridSearchCV.
8. Compared the original and optimized models.

## Model Performance

| Metric | Original Model | Tuned Model |
|---|---:|---:|
| R² Score | 0.6462 | 0.9151 |
| Mean Absolute Error | 47,259.68 | 22,699.21 |
| Tree Depth | 3 | 15 |
| Leaf Nodes | 8 | 1,265 |

**Best Cross-Validation R²:** 0.9062

### Best Hyperparameters

```python
{
    "ccp_alpha": 0.0,
    "max_depth": 15,
    "min_samples_leaf": 5,
    "min_samples_split": 2
}
```

## Key Findings

- House area showed the strongest positive correlation with house prices (0.7565).
- Distance from the city and property age showed negative correlations with prices.
- The initial Decision Tree achieved an R² score of 0.6462.
- Hyperparameter tuning improved the test R² score to 0.9151.
- The Mean Absolute Error decreased by approximately 52%.
- Entropy and Gini Impurity were studied through classification examples, while squared error reduction was used for the regression model.

## How to Run

Clone the repository and open it in VS Code.

Create a virtual environment:

```bash
python -m venv .venv
```

Activate the environment on Windows using Command Prompt:

```cmd
.venv\Scripts\activate.bat
```

Install the required dependencies:

```bash
python -m pip install -r requirements.txt
```

Open `decision_tree.ipynb` in VS Code, select the virtual environment as the Python kernel, and run the notebook cells.

## Conclusion

This project strengthened my understanding of Decision Tree algorithms, splitting criteria, pruning techniques, and hyperparameter tuning.

By applying GridSearchCV, I improved the regression model's predictive performance and gained practical experience in evaluating and optimizing machine learning models.

