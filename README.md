## Predicting High-Value Customers

This project applies logistic regression to classify customers as high-value or low-value based on their purchasing behavior. The objective is to demonstrate how interpretable statistical models can be used in customer analytics.

## Dataset

The dataset includes the following variables:

total_orders: number of orders placed by the customer

avg_order_value: mean value of customer orders

high_value: binary outcome variable (1 = high-value, 0 = low-value)

The dataset was divided into training (80%) and testing (20%) subsets.

## Methodology

Logistic regression was implemented using scikit-learn.

Model performance was evaluated on the test set using accuracy, precision, recall, F1-score, ROC-AUC, and confusion matrix.

Visualizations such as the confusion matrix heatmap, ROC curve, and decision boundary were generated to interpret results.

## Results

The logistic regression model achieved the following performance on the test set:

Accuracy: 0.91

Precision (class 0 – low value): 0.93

Precision (class 1 – high value): 0.85

Recall (class 0): 0.95

Recall (class 1): 0.79

F1-score (class 0): 0.94

F1-score (class 1): 0.81

ROC-AUC: 0.87

## Confusion Matrix
	Predicted Low	Predicted High
Actual Low	78	4
Actual High	6	22

Out of 110 test customers, the model correctly classified 100.

Misclassifications included 4 false positives (low-value predicted as high-value) and 6 false negatives (high-value predicted as low-value).

ROC Curve

The ROC curve indicated strong discriminative performance, with an AUC of 0.87.

At a 0.5 probability threshold, the true positive rate was 0.79 and the false positive rate was 0.05.

Decision Boundary

Customers with both higher total orders and higher average order values were consistently classified as high-value.

Misclassifications occurred mainly in mid-range customers with moderate order frequency and value.

## Interpretation

Logistic regression proved to be an effective baseline classifier with high accuracy.

Precision exceeded recall for the high-value class, showing the model is more cautious in predicting high-value customers.

In business contexts where false positives are costly (e.g., targeting non-high-value customers with promotions), this conservative behavior can be desirable.

Total orders and average order value were both meaningful predictors of customer value.

## Author
**Teerth Gupta**
**Email:** teerthgupta19@gmail.com
**GitHub:** https://github.com/teerthgupta

