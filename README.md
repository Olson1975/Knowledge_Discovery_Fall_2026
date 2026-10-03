## **BAIS:6480 — Data Mining**  
**University of Iowa, Tippie College of Business**  
**Fall 2026**

This repository contains the data preparation and preprocessing code used for **Assignment 2** in BAIS:6480 *Data Mining*. The course focuses on supervised and unsupervised learning techniques, model evaluation, and practical applications of machine learning using real-world datasets.

---

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

### **3. `Assignment2_Notes.md`** *(optional)*  
A summary of the Naive Bayes results, accuracy, confusion matrix, and interpretation.

---

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

If you want, I can also generate:

- a **shorter README**,  
- a **more technical README**,  
- or a **research-style README** that frames the dataset in academic terms.

Just tell me the tone you want.
