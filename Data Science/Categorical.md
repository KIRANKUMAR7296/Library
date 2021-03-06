<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# How to Deal with Categorical Data ?

- **Nominal** : No Ordering | No Ranking among the Values of that `Attribute`. e.g. **Genre** of Music, Movie and Videos
- **Ordinal** : Order | Rank among the Values. e.g. Size of Tshirts ( XS - S - M - L - XL - XXL ), Education Level, Grades 
- You can’t **Train** the Model directly with **Categorical Variables** in their **Raw form**. 
- **Transformation** of **Categorical Labels** in **Numeric Values** by applying some **Encoding** is Important.
- Convert into **Numerical Values**
- Combine `Sparse` Classes ( Classes with very less **Labels** )
- Set **Filter** to Classes ( Class Labels should have atleast **50** Observations )

### Dichotomous
- Male or Female | Yes or No | True or False | 1 or 0

### Logistic Regression
- Classify the Target Variables into Two Classes
- If the Target Variable has more than 2 Classes then Create **Dummy** Variables.
- Combine **Sparse** Categories ( Category Labels with very Less Observations )

### 1. Label Encoding
- Substitute Bins by **Mean** ( e.g. Age Bins by `Mean` of Age Group )
- Label Encoding is Better for `Ordinal` Categories.
- Rank Matters e.g. Designation Feature may contain Labels where Rank Matters ( PHD > Masters > Post Graduate > Bachelor )

> Some times use Business Logic to remove **Redundancy** e.g. Pincode is enough instead of State and City 

### 2. Dummy Coding | One Hot Encoding
- Transform **Non Numerical Labels** to **Numerical Labels** ( **Binary** : `1` or `0` ) 
- Convert a **Categorical Input Variable** into **Numeric Variable**.
- One Hot Encoding is better for `Nominal` Categories ( `Rank` do not Matters )

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
