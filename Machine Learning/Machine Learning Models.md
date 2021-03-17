# Machine Learning Models 🤖🚀💻

<h3><a href=#sup>Supervised Learning</a> : Classify Data or Predict</h3> 

<a href=#linreg><strong>1. Linear Regression</strong></a>&nbsp; |&nbsp; <a href=#logreg><strong>2. Logistic Regression</strong></a>&nbsp; |&nbsp; <a href=#tree><strong>3. Decision Tree<strong></strong></a>&nbsp; |&nbsp; <a href=#forest><strong>4. Random Forest</strong></a>&nbsp; |&nbsp; <a href=#svm><strong>5. Support Vector Machine</strong></a>
 
<h3><a href=#unsup>Unsupervised Learning</a> : Cluster Data </h3> 

![Machine Learning Algorithms](Image/MLAlgorithm.png)

### Steps of Machine Learning
1. Gathering Data
2. Preparing Data ( Preprocessing )
3. Explore Data
4. Clean Data
5. Feature Engineering ( Important Features to Train Model )
6. Choosing a Correct Model
7. Training Data
8. Testing Data and Evaluation
9. Hyperparameter Tuning
10. Prediction

> Model is the system that makes **Predictions**

> **Parameters** are the Factors which are considered by the model to make **Predictions**. **Linear Regression** ( parameters... )

> Learner makes adjustments in the Parameters and the Model to Align the Predictions with Actual Results.

<h1 name='sup'> Supervised Learning</h1>

### A. Regression

- Predict **Dependent Variable** ( **Continuous** ) on the basis of one or more **Independent Features** 
- Find **Relationship** between **Independent Variables** and **Dependent Variable**
- Can be further Improved by **Regularization* or by using **Non Linear Model**

### B. Classififcation

- Predict **Dependent Variable** ( Categories of Labels ) on the basis of **Independent Features**
- Find **Relationship** between **Independent Variable** and **Dependent Variable**
- Output is **Discrete**

<h3 name='linreg'>1. Linear Regression</h3> 

![Linear Regression](Image/RegressionLine.png)

![Equation of Line](Image/EquationLine.png)

> Simple Linear Regression : Find the Line that **Fits** the Data.

> Multiple Linear Regression : Find the Plane | Hyperplane of **Best Fit**.

> Polynomial Regression : Find a Curve for **Best Fit**. 

<h3 name='logreg'>2. Logistic Regression ( Classification )</h3>

- Dependent ( Output ) should be **Discrete** ( 0 or 1 )
- Used for **Classification**
- Probability of Finite Number of Outcomes | Occurence.
- Output values can be between 0 and 1
 
<h3 name='tree'>3. Decision Tree</h3>

- **Root** Node and **Internal** Nodes are **Conditions**
- **Leaf** Node represents a Class **Label** | **Terminal** Node
- **Splits** a Dataset based on **Different** Conditions ( Branch | Edge | Split )
- Used **Binary** Classification and **Multiclass** Classification and even for **Regression**
- Tree Models where the Target Variable takes a **Discrete** Set of Values are **Classification** Tree
- Tree Models where the Target Variable takes a **Continuous** Values are **Regression** Tree
- **CART** : **C**lassification **A**nd **R**egression **T**ree

### Information Gain 

- **Information Gain** is used to decide which Feature ( **Root** Node ) to **Split** on at each step in Building the Tree
- The Split with the Highest **Information Gain** will be taken as the First Split and the process will continue untill **IG** becomes 0

### Gini Index ( Checks for Impurity in the Dataset )

- Lowest Gini Index is selected 
- Pure : All Data belongs to Same Class in a Subset ( Gini Index : 0 )
- Impure : Data is Mixture of Different Classes in a Subset

Advantage of Decision Tree | Disadvantage of Decision Tree
:--- | :---
Handle **Categorical** and **Numerical** Data | Prone to **Overfitting**
No effect of **Outliers** | Need Carefull **Parameter Tuning**

### How to Avoid Overfitting
- Remove | **Prune** Branches with Less Importance ( Irrelevant Feature )
- Early Stop ( Limit the Max Depth of the Tree )

<h3 name='forest'>4. Random Forests ( Ensemble Learning Technique | Bagging )</h3>

- Multiple **Decision Trees** ( Weak Learners ) trained **Parallel** Individually
- **Bootstrapped Data Sets** of Orignal Data and **Randomly** selecting **Subsets** at each step. ( **Sampling** with **Replacement** )
- Bagging Technique ( **Multiple** Decision Trees are **Trained** in **Parallel** to Form a **Strong Learner** ) 
- **Prediction** of Model is based on the **Voting** of Decision Trees Output ( **Majority Voting** )
- Reduces Risk of **Error** and **Overfitting**.

<h3 name='svm'>5. Support Vector Machine</h3>

- Find **Hyperplane** in **N Dimensional Space** that can distinctly classify the data points.
- SVM can be used for both **Regression** and **Classification**
- The Algorithm finds a **Line** or **Hyperplane** that Separates the 2 Classes with Maximum **Margin**.
- **Hyperplanes** are Decision Boundaries that help Classify the Data Points.
- Data Points are **Support Vectors**.
- SVM can be used for **Linear** and **Non Linear** Data.
- SVM can be used as **Kernel Trick** for **Non Linear** Data which Creates a **Hyperplane** in **N Dimensional Space**.

### Benefits 

- SVM also works well with **Unstructured** and **Semi Structured** Data ( Text, Image, Tree )
- **Generalize** Well ( Works well on New Unseen Data )
- Risk of **Overfitting** is Less.

### Disadvantage

- Choosing a Good Kernel Function is not easy
- Long **Training Time** for Large Datasets.
- Difficult to Interpret and Understand Final Model, Variable Weights and Individual Impact.
- Not easy to Fine Tune and Visualize.

### 6. Naive Bayes

- Based on **Conditional Probability** | Class **Prediction** Probability ( Used for **Binary** and **Multiclass** Classification )
- Probabilistic Machine Learning Model ( Likelihood, Prior Probability and Posterior Probability )
- Probability of **Event A** if **Event B** has already occured
- **Naive** : Because it assumes that all of the **Independent Features** are **Independent** from each other

> P( **A** | **B** ) = P( **B** | **A** ) / P( **B** )

All follow Same Process in **Regression** and **Classification** the only difference is Output 

> **Regression** Output : **Continuous**

> **Classification** Output : **Discrete**

<h1 name='unsup'> Unsupervised Learning</h1>

- Find **Patterns** and **Relationships** between **Independent** Features and **Dependent** Feature ( **Labels** )
- Extract Important Features and Explore the Data Set in Detail.

### A. Clustering

- Group the Data Set into Groups | Segments | Clusters According to **Similarity**.
- Customer Segmentation | Fraud Detection | Document Classification

> Clustering Techniques

1. K Mean
- Cluster Data Points with Similar Characteristics in one Cluster
- We Choose **K** number of Clusters
- Select **K** Random Data Points as Centroid
- Data Points nearest to its Corresponding Centroid belongs to that Cluster
- Again the Centroid is Calculated
- The Data Points are Updated based on New Centroid
- **Iterative** Process | Stops when there is no further Classification.
- Different Starting Points ( Random Centroid Selected ) Create Different Clusters 
- **Elbow** Method : Sum of Squared Distance get smaller as the Number of Clusters Increases

2. K Nearest Neighbours
- Calculate Distance between Test Data and Each Row of Training Data
- Sort the Calculated Distance in Ascending Order
- Get Top Rows Nearest to it or most Frequent Classes
- Return the Prediction.

2. Hierarchical

A. Agglomerative
- Bootom Up Approach
- **AGNES** ( **Ag**glomerative **Nes**ting )
- Each Data Point is considered as an Individual Cluster
- At each Iteration, Similar Clusters merge with other Clusters until One Single Cluster remains.

B. Divisive
- Top Down Approach
- **DIANA** ( **Di**vise **Ana**lysis )
- Dividing the Single Cluster into n Clusters

### How we Calculate Similarity between the Clusters
- **MIN** ( Distance between the Closest Points of Two Clusters )
- **MAX** ( Distance between the Farthest Points of Two Clusters )
- Group **AVG** ( Average of Distance between Each Data Points of Two Clusters )
- Distance between **Centroids** ( Distance between the Centroid of Two Clusters )
 
3. Density Based

### B. Dimensionality Reduction

- Aim is to find  the **Inportant Features** that can be used for by our Model for Better Predition.
- Reducing the Number of **Irrelevant Features** that has no relation with the Target Feature.
- There are some Features that brings **Multicollinearity** 
- Feature **Elimination** | **Feature Selection** or Feature **Extraction**
- Save Storage and Time by Improving Performance of Model.
- Due to less number of Features it can be Visualized in 2D and 3D.

### Anomaly Detection :
- Automatically Discover **Unusual** Data Points in Data Set.
- Used to Find Fraudulent Transactions, Identify an Outlier caused by Human Error during Data Entry.
- Reduces Complexity of Data and Helps to Understand Data more Clearly and Better Way.

### Association Mining :
- Set of Items that Frequently Occur together in Data Set.
- Basket Analysis : Items Bought Together | Goods Purchased at the Same Time Help to Develop Marketing Strategies.

### Feature Selection
- **Select** Important Features | Helps to Improve **Accuracy** | Not Every Feature Adds Value to Solve Problem
- **Remove** Unwanted Features | Irrelevant Features Affects Accuracy |
- **Understanding** Each Feature before using it for Creating Machine Learning Model

> Techniques of Dimensionality Reduction

### Feature Extraction

- **PCA** : Principal Component Analysis. ( Reduce Dimensions of Data )
- **LDA** : Linear Discriminant Analysis.
