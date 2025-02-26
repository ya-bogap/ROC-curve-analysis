ROC Curve Analysis of a Scoring Function
Objective
This project evaluates the performance of a scoring function by computing the True Positive Rate (TPR) and False Positive Rate (FPR) at different thresholds. The results are used to generate the Receiver Operating Characteristic (ROC) curve, which helps assess how well the scoring function distinguishes between Positive and Negative data points.

Concept
The scoring function assigns a numeric score to each data point. By setting different score thresholds, we classify data points as either Positive or Negative and measure:

TPR (Sensitivity): The proportion of actual positives correctly identified.
FPR (False Alarm Rate): The proportion of actual negatives incorrectly classified as positives.
The ROC curve visualizes the trade-off between TPR and FPR at different thresholds. The Area Under the Curve (AUC) provides a single metric summarizing the performance of the scoring function.

Dataset
The dataset consists of 20 data points:

10 Positive samples
10 Negative samples
Each sample has an associated score from the scoring function.
No.	Label	Score
1	Positive	25
2	Positive	21
3	Positive	20
4	Positive	19
5	Positive	18
6	Positive	17
7	Positive	14
8	Positive	13
9	Positive	10
10	Positive	5
11	Negative	18
12	Negative	15
13	Negative	13
14	Negative	12
15	Negative	10
16	Negative	8
17	Negative	5
18	Negative	4
19	Negative	3
20	Negative	3

Methodology
Compute TPR and FPR for thresholds between 3 and 25.
Plot the ROC curve by plotting TPR (Y-axis) vs. FPR (X-axis).
Calculate the AUC (Area Under the Curve) as a single performance metric.

Run the Python Script

Expected Output
Printed Table of Thresholds, FPR, and TPR


Thresholds | FPR | TPR
inf        | 0.00 | 0.00
25.00      | 0.00 | 0.10
19.00      | 0.00 | 0.40
18.00      | 0.10 | 0.50
17.00      | 0.10 | 0.60
15.00      | 0.20 | 0.60
14.00      | 0.20 | 0.70
13.00      | 0.30 | 0.80
12.00      | 0.40 | 0.80
10.00      | 0.50 | 0.90
8.00       | 0.60 | 0.90
5.00       | 0.70 | 1.00
4.00       | 0.80 | 1.00
3.00       | 1.00 | 1.00

ROC Curve

The ROC curve will be displayed with the blue line representing model performance.
The dashed gray line represents random guessing.
The AUC score is displayed in the legend.
Interpretation of Results
ROC Curve Analysis:

The closer the curve is to the top-left corner, the better the model.
The AUC = 0.83, meaning the scoring function has good but not perfect performance.
If AUC was near 1.0, the model would be perfect.
If AUC was near 0.5, the model would be as bad as random guessing.
Choosing a Threshold:

If we prioritize catching all positives (high sensitivity) → Choose a low threshold.
If we prioritize avoiding false alarms (high specificity) → Choose a high threshold.
