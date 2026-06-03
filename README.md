# Developer Salary Insights - StackOverflow Survey 2024 Analysis

This project is part of the Data Science Nanodegree Capstone. It applies the **CRISP-DM** (Cross-Industry Standard Process for Data Mining) methodology to analyze the StackOverflow Developer Survey 2024 dataset, focusing on key drivers of developer compensation worldwide.

---

## 1. Project Motivation
The goal of this project is to understand the economic landscape of modern software development and build a machine learning model capable of predicting annual compensation. To guide the analysis, three core questions were investigated:
1. **Tech-Stack Impact:** Does incorporating Python into your stack yield a significant financial advantage?
2. **Work Modality:** How does the modern tech workforce split between Remote, Hybrid, and In-Person roles, and do remote workers earn a premium?
3. **Predictive Modeling:** Can we accurately predict a developer's salary based purely on their location, professional experience, and work modality?

---

## 2. Installation & Libraries
The analysis was built using Python within a Windows Subsystem for Linux (WSL) environment. 

To run the Jupyter Notebook, you need the following Python standard libraries and data science packages installed:
* `numpy`
* `pandas`
* `matplotlib`
* `seaborn`
* `scikit-learn`

The dataset is streamed directly from source via URL.

---

## 3. File Descriptions
* **`DataScienceBlogNB.ipynb`**: The core executable script containing the complete technical implementation of the CRISP-DM process, including initial data exploration (EDA), rigorous data cleaning (outlier removal via quantiles, type casting), model training, and evaluation.
* **`README.md`**: This file, providing a high-level technical overview and summary of findings.

---

## 4. Summary of Analysis & Results

### Data Preparation Highlights
* Filtered out incomplete records lacking valid target (`ConvertedCompYearly`) and experience (`YearsCodePro`) fields.
* Handled severe salary outliers by trimming data outside the 1st and 99th percentiles to avoid skewing ML models.
* Encoded complex string features into numeric formats using One-Hot encoding.

### Core Findings
* **The Python Premium:** Developers actively utilizing Python in their stack show a noticeably higher median salary globally ($67,666 USD vs. $64,444 USD), reinforcing Python's leverage in high-paying sectors like Data Science and AI.
* **Work Modality Shifts:** Remote and hybrid work models dominate the modern tech landscape. Fully remote roles tend to cluster around higher compensation bands.
* **Model Performance:** The trained `RandomForestRegressor` achieved an **R²-Score of 0.5243**, explaining 52.43% of the salary variance with a Mean Absolute Error (MAE) of **$29,716.21 USD**.
* **Scenario Prediction:** For a simulated developer based in Germany with 5 years of professional experience working fully remote, the model predicts a fair market salary of **$76,751.68 USD**.

---
You can read the full, non-technical blog post here: https://medium.com/@pascal_28740/code-kohle-homeoffice-was-bestimmt-das-gehalt-in-der-tech-welt-wirklich-4b395d0c031a

## 5. Licensing, Authors, & Acknowledgements
* **Author:** Pascal Porteset
* **Data Source:** Special thanks to StackOverflow for making the annual Developer Survey public. 
* **License:** MIT License.
