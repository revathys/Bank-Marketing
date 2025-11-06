# Bank Marketing

# <ins> **Business Understanding** </ins>

The goal of this project was to build predictive models using the UCI Bank Marketing dataset to identify customers most likely to subscribe to a term deposit . The key objective for business impact is to **maximize recall** — ensuring that we correctly identify as many potential subscribers as possible while minimizing wasted marketing efforts.


Please find the Jupyter note [here](https://github.com/revathys/Bank-Marketing/blob/main/prompt_III.ipynb).

## Model Candidates & Evaluation Metrics
Models evaluated using **3-fold cross-validation** and **GridSearchCV** optimization on recall:
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Linear Support Vector Machine (SVM)

**Evaluation Metrics:**
- Accuracy
- Recall
- Training time


## <ins>**Business Recommendations**</ins>

1. **Target high-probability clients** — focus marketing efforts on customers resembling prior successful subscribers (e.g., positive past campaign outcome, higher education, contacted via cellular).
2. **Campaign Timing Optimization** — certain months (May, July, August) correlate with higher success; align campaigns accordingly.

## <ins>**Summary of Findings**</ins>
 - Linear SVM has the best Recall, though it took the most train time.
  - Recall improved significantly over baseline and initial run without hyperparameter grids.
  - False positives moderately increased but acceptable trade-off for improved marketing reach
- **Top Predictors (Feature importance):**
  1. emp.var.rate    
  2. month    
  3. cons.price.idx  
  4. euribor3m
  5. education
  6. contact
     

| Model                | Best Params                                                      | Train Time (s) | Train Accuracy | Test Accuracy | Recall |
|----------------------|------------------------------------------------------------------|----------------|----------------|----------------|---------|
| Logistic Regression  | {'classifier__C': 10, 'classifier__penalty': 'l2'}               | 11.45          | 0.912          | 0.911          | 0.702   |
| KNN                  | {'classifier__n_neighbors': 3}                                   | 30.93          | 0.941          | 0.896          | 0.696   |
| Decision Tree        | {'classifier__max_depth': 3, 'classifier__min_samples_split': 2} | 19.07          | 0.909          | 0.909          | 0.771   |
| Linear SVM           | {'classifier__C': 10, 'classifier__class_weight': 'balanced'}    | 10.32          | 0.860          | 0.857          | 0.868   |


   



