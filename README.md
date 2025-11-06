# Bank Marketing

# <ins> **Business Understanding** </ins>

The goal of this project was to build predictive models using the UCI Bank Marketing dataset to identify customers most likely to subscribe to a term deposit . The key objective for business impact is to **maximize recall** — ensuring that we correctly identify as many potential subscribers as possible while minimizing wasted marketing efforts.


Please find the Jupyter note [here](https://github.com/revathys/Bank-Marketing/blob/main/prompt_III.ipynb).

## Model Candidates & Evaluation Metrics
Models evaluated using **3-fold cross-validation** and **GridSearchCV** optimization on recall_macro:
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Linear Support Vector Machine (SVM)

**Evaluation Metrics:**
- Accuracy
- Recall
- Training time

  Model                     | Train Time (s) | Train Accuracy | Test Accuracy | Recall
  -------------------------------------------------------------------------------------
 Logistic Regression        |      8.01      |     0.912      |     0.911     | 0.702
 KNN                        |     31.06      |     0.941      |     0.896     | 0.696
 Decision Tree              |     18.14      |     0.909      |     0.909     | 0.771
 Linear SVM                 |     11.70      |     0.860      |     0.857     | 0.868


     
1. **Target high-probability clients** — focus marketing efforts on customers resembling prior successful subscribers (e.g., positive past campaign outcome, higher education, contacted via cellular).
2. **Campaign Timing Optimization** — certain months (May, August) correlate with higher success; align campaigns accordingly.
 
## <ins>**Summary of Findings**</ins>

1. **Target high-probability clients** — focus marketing efforts on customers resembling prior successful subscribers (e.g., positive past campaign outcome, higher education, contacted via cellular).
2. **Campaign Timing Optimization** — certain months (May, August) correlate with higher success; align campaigns accordingly.



