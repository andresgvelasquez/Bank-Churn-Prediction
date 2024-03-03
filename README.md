# Beta Bank: Will a Customer Leave the Bank Soon?

## Contact
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/andres946/)
[![Correo Electrónico](https://img.shields.io/badge/Correo%20Electrónico-andresgvelasquez8@gmail.com-red?style=for-the-badge&logo=mail.ru)](mailto:andresgvelasquez8@gmail.com)  

## Description of the project:
Beta Bank customers are gradually leaving, month by month. Bankers have discovered that it is cheaper to retain existing customers than to attract new ones.
We need to predict if a customer will leave the bank soon. You have data on customers' past behavior and termination of contracts with the bank.
Create a model with the maximum possible F1 score. To pass the review, you need an F1 score of at least 0.59. Verify F1 for the test set.
Additionally, you must measure the AUC-ROC metric and compare it with the F1 score.

## Data Description

**Location:** `../datasets/Churn.csv`

**Features:**
- `RowNumber`: index of the data row
- `CustomerId`: unique customer identifier
- `Surname`: last name
- `CreditScore`: credit score
- `Geography`: country of residence
- `Gender`: gender
- `Age`: age
- `Tenure`: period for which the customer has held a fixed-term deposit (years)
- `Balance`: account balance
- `NumOfProducts`: number of bank products used by the customer
- `HasCrCard`: whether the customer has a credit card (1 - yes; 0 - no)
- `IsActiveMember`: customer activity (1 - yes; 0 - no)
- `EstimatedSalary`: estimated salary

**Target:**
- `Exited`: Whether the customer has left (1 - yes; 0 - no)

## Virtual Environment Setup

To run this project, it is recommended to create a Python virtual environment. You can do this by executing the following commands in your terminal:

```bash
python -m venv venv
source venv/bin/activate  # For Linux/Mac
# or
.\venv\Scripts\activate   # For Windows
```

Then, you need to install the dependencies:

```bash
pip install -r requirements.txt
```
Once you have set up the virtual environment and installed the dependencies, you can run the project.

## Metrics

**F1 Score**:
A metric combining precision and recall, useful for evaluating binary classification models.

**ROC-AUC**:
Evaluates the discrimination ability of a classification model by measuring the area under the ROC curve.

All models show improvement after adjusting for class weight and balancing for F1 and ROC-AUC metrics. The model with the best F1 score was selected, which corresponds to the random forest with weight adjustment, balancing, and threshold adjustment.

|  Model             | Weight Adjustment | Balancing   | Threshold | F1       | ROC-AUC  |
|--------------------|-------------------|-------------|-----------|----------|----------|
| Logistic Regression| No                | No          | 0.50      | 0.3201   | 0.7945   |
| Logistic Regression| balanced          | upsampled   | 0.50      | 0.9298   | 0.9241   |
|  Decision Tree     | No                | No          | 0.50      | 0.5557   | 0.7945   |
|  Decision Tree     | balanced          | upsampled   | 0.50      | 0.9298   | 0.9242   |
|  Random Forest     | No                | No          | 0.50      | 0.5794   | 0.8504   |
|  Random Forest     | balanced          | upsampled   | 0.44      | 0.9600   | 0.9969   |

## Conclusion