# How to Deal with Outliers ?

### Outliers
- **Data Point** that differs significantly from other **Observations** in the Dataset.
- Outliers in a **Dataset** can **Skew** the Data and lead to make Decisions based on **Faulty Data**.

### Cause of Outliers
1. Human Error ( Data Entry )
2. Measurement ( Instrumental )
3. Experimental ( Data Extraction )
4. Natural Case ( Special Unique Case )

In Machine Learning and in any **Quantitative Analysis** the **Quality** of Data is as important as Quality of **Prediction** or **Classification** Model.

How many **Features** to take into account to **Detect Outliers** ?
- **Univariate** | **Multivariate**

> **Data Visualization** is a most important part that plays the role of communicating with Data and Visualize Outlier.

> **Boxplot**, **Scatter Plot** and **Histograms** are better plots to Find Outliers in the Data Set.

### Methods for Outlier Detection

### 1. Z Score or Extreme Value Analysis
- How many **Standard Deviations** a **Data Point** is from the **Sample's Mean**
- **z** = ( x - **mean** ) / **standard deviation**
- Data Points after **3 Standard Deviations** ( mean +- 3 * std ) are considered as **Outliers**.

> **Solution** : Apply Transformation of Data : Scaling

### ( DBSCAN ) | Density Based Spatial Clustering of Applications with Noise
- **Clustering** methods are useful tools that helps us to **Visualize** and **Understand** Data better.
- Relationships between **Features** can be represented via **Clustering**.
- **DBSCAN** is a **Density Based Clustering Algorithm**, it is focused on finding **Neighbors** by **Density**.
- Outlier lies in No Cluster it is Seperate from every other Data point.

### How to Deal with Outliers ?

1. Setup a **Filter** and **Trim** Data Set.
2. Remove the Outlier if it is very Small.
3. **Inter Quartile** Range 
4. Change the Value of Outlier or Replace it with something Meaningful.

### Five Number Summary

> Divide the Data into 4 Equal Quarters

1. Minimum : **Smallest** value in a Dataset.
2. 1<sup>st</sup> **Quartile** ( **Q1** ) | 25<sup>th</sup> **Percentile** : 25% of Data Values are smaller and 75% are larger.
3. 2<sup>nd</sup> **Quartile** ( **Q2** ) | 50<sup>th</sup> **Percentile** : **Median** | 50% of Data Values are smaller and 50% are larger the Median.
4. 3<sup>rd</sup> **Quartile** ( **Q3** ) | 75<sup>th</sup> **Percentile** : 75% of Data Values are smaller and 25% are larger.
5. Maximum : **Largest** Value in a Dataset.

> **Five Number Summary** can be visually represented using **Boxplot**.
- Horizontal Line on both ends of Boxplots are **Whiskers**.
- Box is called **Interquartile Range** ( **IQR** ).
- **IQR = Q3 - Q1** 

> Data Value is considered as **Outlier** 
- Data Value **<** Q1 - 1.5 * ( **IQR** ) 
- Data Value **>** Q3 + 1.5 * ( **IQR** ) 

> **Outlier** is represented by dot ( **.** ) in **Boxplot**  