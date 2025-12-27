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
This project focuses on improving street lighting efficiency and enhancing commuter safety by detecting, analysing, and responding to lighting faults. Using a synthetic dataset of 466 lighting records, the system identifies potential issues, predicts their severity, and classifies fault types to suggest automated responses.

## Key Features

### Data Cleaning

I preprocessed the dataset to ensure high-quality input for the models.
* **Feature Engineering:** Converted raw timestamps into time features.
* **Standardisation:** Handled missing values and standardised location names across Singapore districts.

### Fault Analysis
I explored the dataset using Exploratory Data Analysis (EDA) to find patterns in streetlight failures.
* **Visualisation:** Created charts to show which areas have the most streetlight faults.
* **Tools:** Used pandas to organise the data and seaborn to draw charts of the trends.


### Severity Prediction
To prioritize maintenance, I built a model to identify the severity of each fault.
* **Model:** Decision Tree Classifier
* **Outcome:** The system labels faults as critical, high, medium, or low, ensuring that the most serious issues are addressed first.


### Fault Classification
Each fault is categorised into specific technical types to indicate the appropriate tools or actions required.
* **Categories:** Control System, Power-Related, and Sensor-Related failures.
* **Validation:** Used confusion matrices to ensure the model correctly distinguishes between hardware failure and signal noise.

### Automated Response
The final stage of the pipeline transforms data into action.
* **Logic:** The system filters for critical faults and generates immediate alerts.
* **Impact:** Reduces manual monitoring and ensures faster response times for public safety.

---
### Tech Stack
- **Languages:** Python
- **Libraries:** Scikit-Learn, Pandas, Matplotlib, Seaborn
- **Model:** Decision Tree Classification

**[View the Full Code on GitHub](https://github.com/shiyunx/lighting-fault-detection)**