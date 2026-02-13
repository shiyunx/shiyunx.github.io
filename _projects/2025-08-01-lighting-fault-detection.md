---
layout: post
title: Lighting Fault Detection
date: 2025-08-01
description:
repo:
category: Data
permalink: /projects/2025-08-01-lighting-fault-detection/
---

## Objective
This project focuses on improving street lighting efficiency and enhancing commuter safety by detecting, analysing, and responding to lighting faults. Using a dataset of 466 lighting records, the system identifies potential issues, predicts their severity, and classifies fault types to suggest automated responses.

## Key Features

### Data Cleaning
I preprocessed the dataset to ensure high-quality input for the models.
* **Feature Engineering:** Converted raw timestamps into time features.
* **Standardisation:** Handled missing values and standardised location names across Singapore districts.

### Fault Analysis
I explored the dataset using Exploratory Data Analysis (EDA) to find patterns in streetlight failures.
* **Visualisation:** Created charts to show which areas have the most streetlight faults.
* **Tools:** Used Pandas to organise the data and Seaborn to draw charts of the trends.

### Severity Prediction
To prioritize maintenance, I built a model to identify the severity of each fault.
* **Outcome:** The system labels faults as critical, high, medium, or low, ensuring that the most serious issues are addressed first.

### Fault Classification
Each fault is categorised into specific technical types to indicate the appropriate tools or actions required.
* **Categories:** Control System, Power-Related, and Sensor-Related failures.
* **Check:** Used confusion matrices to ensure the model correctly distinguishes between hardware failure and signal noise.

### Automated Response
The final stage of the pipeline turns insights into actions.
* **Process:** The system filters for critical faults and generates immediate alerts.
* **Outcome:**  Helps reduce manual monitoring and allows faster response times.

### Tools & Skills
- **Language:** Python
- **Data:** Pandas, Matplotlib, Seaborn
- **Machine Learning:** Scikit-Learn
- **Model:** Decision Tree Classifier

[View Github](https://github.com/shiyunx/lighting-fault-detection)