# SVM

🧪 Methodology
1. Dataset Selection & Preprocessing
A multi-class dataset from the UCI library was used.

The dataset had between 5k to 30k rows.

The dataset was split into 10 random 70-30 train-test splits, labeled S1 to S10.

2. Model and Hyperparameter Optimization
Support Vector Machine (SVM) was chosen as the classifier.

We used Optuna, a hyperparameter optimization library, to tune:

Kernel type (rbf or poly)

Regularization parameter C

gamma (kernel coefficient for ‘rbf’ and ‘poly’)

Each sample was optimized over 100 iterations using Optuna’s study.optimize() function.

3. Evaluation
For each sample, the best accuracy and corresponding SVM parameters were recorded.

The sample with the highest accuracy was further analyzed by plotting a convergence graph.

📋 Results Table

Sample	Best Accuracy (%)	Best SVM Parameters
S1	63.54	Kernel: rbf, C: 8.811, Gamma: 0.00298
S2	61.25	Kernel: rbf, C: 3.0188, Gamma: 0.09086
S3	60.42	Kernel: rbf, C: 1.7888, Gamma: 0.05165
S4	66.88	Kernel: rbf, C: 49.4097, Gamma: 0.06708
S5	64.38	Kernel: rbf, C: 6.0602, Gamma: 0.04667
S6	65.42	Kernel: rbf, C: 4.6435, Gamma: 0.08755
S7	63.96	Kernel: poly, C: 95.3259, Gamma: 0.02517
S8	63.33	Kernel: rbf, C: 31.381, Gamma: 0.09886
S9	63.96	Kernel: rbf, C: 2.4908, Gamma: 0.05054
S10	65.21	Kernel: rbf, C: 12.8308, Gamma: 0.0682
📈 Convergence Graph (Best Sample: S4)
This graph shows how accuracy improved over 100 iterations during Optuna optimization for the best-performing sample S4.

The blue points represent the objective (accuracy) values at each iteration.

The red line tracks the best value so far, giving insight into convergence behavior.


As seen above, performance quickly improved within the first 20 iterations, gradually converging to the optimal value (~66.88%).
