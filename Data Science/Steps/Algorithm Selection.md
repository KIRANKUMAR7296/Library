<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Algorithm Selection

### Why Linear Regressions is Flawed ?
- Simple Linear Regression Model fit a **Straight Line** ( **Hyperplane** for Muliple Variables ) 
- Easy to **Interpret** and **Understand**
- Prone to **Overfitting** with many Features and cannot Express Non Linear Relationship

### Regularization can Improve Regression
- If we a Fit Regression Model on 100 Features ( Training )
- Each Coefficient will Memorize each Observations ( Learn Pattern including **Noise** )
- The Model would have Perfect Accuracy on the Training Data but it will not Generalize well on Test Data ( New Unseen Data )
- Regularization can Prevent **Overfitting** by Artificially Penalizing Model Coefficient
- It can **Discourage** Large Coefficients
- It can **Remove** Features Completely ( Setting Coefficients to 0 )
- It can **Encourage** Small Coefficients

> Loss = Sum of Square **Residual** ( Actual - Prediction ) <sup>2</sup> 

LASSO ( `L1` ) | Ridge ( `L2` ) | Elastic ( `L1` + `L2` )
:--- | :--- | :---
Least Absolute Shrinkage Selection Operator | Mountain Ridges | Between LASSO and Ridge  
Loss + lambda * \| slope \| | Loss + lambda *  ( slope ) <sup>2</sup> | Loss + lambda1 * \| slope \| + lambda2 * ( slope ) <sup>2</sup>
`Absolute` of Coefficient | `Square` of Coefficients | Mix of `Absolute` and `Square`
Can lead Coefficient to Exactly Zero | Lead to Small Coefficient but not Zero | No Zero 
Feature **Selection** and Feature **Elimination** | Feature **Shrinkage**

### Decision Trees
- Prone to **Overfit** with many inputs

> **Base Models** are **Decision Trees**

Bagging | Boosting
:--- | :---
Reduce Chance of `Overfitting` | Improve the `Prediction` \| `Classification` of Model
Trains Large Number of `Individiual` Learners in `Parallel` | Trains a Large number of `Weak` Learners in `Sequence`
Uses `Complex Base Models` and tries to `Simplify` their Predictions | Uses `Simple Base Models` and tries to `Improve`
Each `Tree` is `Random` Subset of Features ( **Feature Selection** ) and Observations ( **Resmapling** ) | Each Tree in the `Sequence` tries to `Correct` the Prediction Errors of the Previous Tree 
Don't have many Complicated Parameters to Tune | More Complicated to Tune

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
