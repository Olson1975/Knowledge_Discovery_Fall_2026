## **BAIS:6480 — Data Mining**  
**University of Iowa, Tippie College of Business**  
**Fall 2026**

This repository contains the data preparation and preprocessing code used for in BAIS:6480 *Data Mining*. The course focuses on supervised and unsupervised learning techniques, model evaluation, and practical applications of machine learning using real-world datasets.

---


---

## **Dataset Description**

The dataset used in this assignment is a **historical linked census dataset (1900–1910)** created for research on internal migration and occupational mobility. The raw dataset includes:

- Individual demographic attributes  
- Household and geographic identifiers  
- Occupational information  
- Linkage indicators between census years  
- Derived variables created during preprocessing  

The cleaned dataset produced here is the version used for the Naive Bayes classification task.

---

## **Repository Contents**

### **1. `preprocessing.ipynb` / `preprocessing.py`**  
This file contains all data cleaning and transformation steps, including:

- Loading the raw full-count census microdata  
- Handling missing values  
- Standardizing categorical variables  
- Creating derived fields needed for classification  
- Filtering records to include only linked individuals  
- Exporting the final dataset for Weka (`.csv` or `.arff`)

### **2. `cleaned_dataset.csv`**  
The final dataset produced by the preprocessing script. This is the dataset used in Weka for Assignment 2.

### **3. `Assignment2_Notes.md`**  
A summary of the Naive Bayes results, accuracy, confusion matrix, and interpretation.

### **4. `Assignment 3`**

## **Assignment 2 Overview**

Assignment 2 requires students to:

1. Prepare a dataset for classification.  
2. Run a **Naive Bayes classifier** in **Weka Explorer** using **10‑fold cross‑validation**.  
3. Report:
   - Estimated accuracy  
   - Confusion matrix  
   - A brief interpretation of results  
4. Discuss whether the model performance is “good” and whether it would be satisfactory for the intended analytical purpose.

This repository contains the preprocessing code used to generate the cleaned dataset required for the Naive Bayes model.

---
## **Assignment 3**: 

Decision Trees, Pruning, and Model Comparison
This assignment extends my analysis of internal migration in the linked 1850–1870 U.S. Census data, using demographic, disability, household, occupation, birthplace, and parental characteristics to predict whether an individual moved between linked census observations. The underlying project dataset contains more than 34 million records, making computational feasibility an important part of the modeling process.

Following feedback from Assignment 2, I revised the dataset to retain additional potentially meaningful variables while correcting categorical features that had previously been represented as numeric values. Missing information was explicitly represented using categories such as Missing and NoParent, and categorical predictors were one-hot encoded for use with scikit-learn. Because fitting and repeatedly evaluating unrestricted decision trees on the entire dataset was computationally prohibitive, the Assignment 3 experiments use a reproducible random sample of 100,000 observations.

The assignment explores three major areas:

_Default/unpruned decision tree_: The initial tree grew to 37,397 nodes and 18,699 leaves, illustrating substantial model complexity and overfitting. AGE was the strongest feature in the unpruned model, with occupation, missing nativity, and missing literacy also contributing substantially.

_Cost-complexity pruning_: A reduced grid of ccp_alpha values was evaluated using cross-validation. The selected value, approximately 0.0013355, reduced the tree to just 39 nodes and 20 leaves while achieving approximately 70.7% cross-validated accuracy. The strongest features in the pruned model included AGE, NATIVITY_Missing, and LIT_Missing.

_Model comparison_: The decision-tree results are compared with the Naive Bayes work from Assignment 2. The earlier Naive Bayes model achieved approximately 61.6% accuracy, providing a useful baseline for evaluating whether the additional flexibility of a decision tree improves prediction of movement.
The assignment also investigates why missing nativity became an important feature, examining its relationship with race, age, and urban/rural residence and using a chi-square test to evaluate the relationship between race and nativity missingness. In the 100,000-record sample, that test produced χ² = 5.04, p ≈ 0.169, so the racial differences in nativity missingness were not statistically significant at the 0.05 level.

Finally, the assignment includes a decision tree constructed by hand using information gain, demonstrating the entropy and information-gain calculations underlying the algorithm rather than treating the decision-tree classifier solely as a black box.

Key concepts: 
Decision Trees 
· Entropy 
· Information Gain 
· Cost-Complexity Pruning 
· Cross-Validation 
· Naive Bayes 
· Categorical Encoding 
· Historical Census Data 
· Migration 
· Python 
· scikit-learn

_**Main notebook: a3_decision_tree_experiments.ipynb**_


## **Purpose of This Repository**

This repository documents the full data preparation workflow for Assignment 2. The goal is to provide a reproducible pipeline that:

- Cleans and structures the historical census dataset  
- Produces a classification-ready file for Weka  
- Supports analysis of occupational mobility using Naive Bayes  

The preprocessing code ensures that the dataset is consistent, complete, and formatted correctly for machine learning tasks.

---

## **Course Learning Objectives Demonstrated**

- Data cleaning and preprocessing for machine learning  
- Understanding classification algorithms  
- Evaluating model performance  
- Interpreting confusion matrices  
- Applying cross-validation  
- Working with large, complex historical datasets  

---

## **Author**

**Karin Ulery**  
Graduate Researcher — Geo-Social Lab  
University of Iowa  
Fall 2026

---


