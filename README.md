# Patient Intelligence Pipeline: Time Series Analysis, Similarity Search & Clinical Diagnosis Classification

## Overview

This project implements a complete Patient Intelligence Pipeline for predictive healthcare analytics using a simulated patient monitoring dataset. The system combines Time Series Analysis, Trend Detection, Similarity Search, and Supervised Machine Learning techniques to identify deteriorating patient conditions, discover clinically similar patient profiles, and automatically classify patient diagnoses from historical vital sign data.

Developed as part of **DS-3002 Data Mining – Assignment #3 (Spring 2026)** at FAST-NUCES.

---

## Objectives

The project addresses three major healthcare analytics challenges:

1. Detect trends and anomalies in patient vital signs over time.
2. Identify clinically similar patients using distance-based similarity measures.
3. Build and compare multiple machine learning models for automated diagnosis prediction.

---

## Dataset

**Dataset:** Simulated Patient Vitals Dataset

**Characteristics:**

* Approximately 60,000 records
* 500 patients
* Around 120 readings per patient
* Readings collected every 6 hours over 30 days

### Features

| Feature                | Description                  |
| ---------------------- | ---------------------------- |
| PatientID              | Anonymous patient identifier |
| Timestamp              | Reading timestamp            |
| HeartRate              | Heart rate (bpm)             |
| BloodPressureSystolic  | Systolic blood pressure      |
| BloodPressureDiastolic | Diastolic blood pressure     |
| BloodOxygenLevel       | Oxygen saturation (%)        |
| BodyTemperature        | Body temperature (°C)        |
| RespiratoryRate        | Breaths per minute           |
| SleepHours             | Hours slept                  |
| StressLevel            | Stress score (1–10)          |
| Age                    | Patient age                  |
| Gender                 | Patient gender               |
| Diagnosis              | Target class label           |

### Diagnosis Classes

* Healthy
* Hypertension
* Diabetes
* Arrhythmia
* Sleep Disorder


---

## Data Preprocessing

The preprocessing pipeline performs:

* Timestamp parsing and validation
* Missing value detection
* Physiological range filtering
* Dataset cleaning
* Patient-wise time series construction
* Feature engineering

### Patient-Level Features

For each patient and vital sign:

* Mean
* Standard Deviation
* Minimum
* Maximum
* Linear Trend Slope

These features are used for similarity search and classification tasks.

---

## Part A: Time Series Analysis & Trend Detection

### Techniques

* Heart Rate Time Series Visualization
* Descriptive Statistics
* Coefficient of Variation Analysis
* Moving Average Smoothing
* Time Series Decomposition
* Trend Detection
* Statistical Anomaly Detection

### Methods

* 7-point Rolling Mean
* 14-point Rolling Mean
* Additive Seasonal Decomposition
* Personal Threshold Anomaly Detection (μ ± 2σ)

### Outputs

* Patient trend visualizations
* Trend analysis reports
* Anomaly summaries
* Clinical interpretation of detected patterns

---

## Part B: Similarity Search & Patient Matching

### Distance Metrics

* Euclidean Distance
* Manhattan Distance

### Time Series Similarity

* Dynamic Time Warping (DTW)

### Applications

* Nearest-neighbour patient retrieval
* Clinical case matching
* Risk profile identification
* New patient diagnosis support

---

## Part C: Supervised Classification

Five machine learning models are implemented and compared.

### 1. Decision Tree

* Entropy or Gini criterion
* Depth tuning
* Feature importance analysis

### 2. Rule-Based Classification

* Decision tree rule extraction
* Interpretable clinical rules

### 3. k-Nearest Neighbour (kNN)

* Hyperparameter tuning
* Euclidean vs Manhattan comparison

### 4. Naïve Bayes

* Gaussian Naïve Bayes
* Feature distribution analysis

### 5. Support Vector Machine (SVM)

* One-vs-Rest multiclass strategy
* RBF Kernel
* Polynomial Kernel
* Cross-validation tuning

---

## Evaluation Metrics

Each classifier is evaluated using:

* Accuracy
* Precision (Macro)
* Recall (Macro)
* F1 Score (Macro)
* Confusion Matrix

---

## Technologies Used

* Python 3.x
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Statsmodels
* dtaidistance
* tslearn
* imodels

---

## Installation

```bash
git clone https://github.com/your-username/patient-intelligence-pipeline.git

cd patient-intelligence-pipeline

pip install -r requirements.txt
```

---


## Expected Outcomes

The completed pipeline provides:

* Detection of abnormal patient trajectories
* Identification of clinically similar patients
* Automated diagnosis prediction
* Comparative evaluation of classical machine learning approaches
* Explainable decision support for healthcare analytics

---


## License

This project is developed for educational and academic purposes only.



FAST-NUCES
