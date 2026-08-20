# Speech-Based Ayurvedic Prakriti Prediction

## Project Overview

This research project explores a machine learning–based approach for predicting Ayurvedic Prakriti types — **Vata, Pitta, and Kapha** — using speech signal analysis.

The study investigates whether acoustic characteristics present in human speech can be used as computational features for Prakriti classification. The work focuses on developing a subject-level machine learning pipeline, with particular attention to feature engineering, model evaluation, and prevention of data leakage.

The results demonstrate the potential of speech-based features as an assistive computational approach for exploring objective Prakriti classification.

<br>

## Research Internship

This project was carried out as part of a **Research Internship in AI/ML** at **Indian Institute of Information Technology Dharwad (IIIT Dharwad)**, in collaboration with the **Department of Electronics and Communication Engineering**.

The research work involved the analysis of real-world speech data, acoustic feature extraction, statistical feature engineering, machine learning model development, and subject-level evaluation.

> **Research Internship Project — AI/ML**  
> **Institution:** Indian Institute of Information Technology Dharwad  
> **Duration:** September 2025 – February 2026  
> **Team Size:** 4 Members  
> **Technologies:** Python, Exploratory Data Analysis (EDA), eGeMAPS, Machine Learning

<br>

## Objectives

- Investigate the feasibility of using speech signals for Ayurvedic Prakriti classification
- Extract acoustic characteristics from speech recordings using eGeMAPS
- Develop a machine learning pipeline for classifying Vata, Pitta, and Kapha
- Perform subject-level feature aggregation to prevent data leakage
- Evaluate model performance using group-based cross-validation

<br>

## Methodology

### 1. Speech Data Collection

Real-world speech recordings were collected from participants, with multiple recordings obtained from individual subjects.

The recordings were processed to extract acoustic features for subsequent machine learning analysis.

### 2. Acoustic Feature Extraction

Acoustic features were extracted using the **extended Geneva Minimalistic Acoustic Parameter Set (eGeMAPS)**.

These features capture various characteristics of speech, including spectral, temporal, and prosodic properties.

### 3. Feature Aggregation

Since multiple recordings were available for individual participants, statistical aggregation was performed at the **participant level**.

The extracted features were summarized using statistical measures such as:

- Mean
- Standard deviation
- Minimum
- Maximum

This ensured that the final feature representation corresponded to individual subjects rather than individual recordings.

### 4. Model Development

A **Random Forest classifier** with balanced class weights was trained on the aggregated feature set to classify the three Prakriti categories:

- Vata
- Pitta
- Kapha

### 5. Evaluation Strategy

A subject-level evaluation strategy was adopted to reduce the possibility of data leakage.

The evaluation included:

- Subject-level train-test split
- 5-fold **GroupKFold cross-validation**
- Accuracy
- Balanced accuracy
- Weighted F1-score
- Comparative evaluation with other machine learning approaches

### Why GroupKFold?

When multiple recordings are available from the same participant, a conventional random train-test split can result in recordings from the same person appearing in both training and testing data.

This can lead to data leakage and overly optimistic performance estimates.

**GroupKFold** ensures that all recordings belonging to a participant remain within the same fold, providing a more reliable estimate of subject-level generalization.

<br>

## Results

The Random Forest model demonstrated strong performance on the evaluated dataset:

| Metric | Performance |
|--------|-------------|
| Test Accuracy | **95.89%** |
| Balanced Accuracy | **98.21%** |
| Weighted F1-Score | **96.00%** |

The Random Forest approach also demonstrated stronger performance than the evaluated neural-network-based approaches, including **Multi-Layer Perceptron (MLP)** and **Feed-Forward Neural Network (FNN)** models.

> **Note:** Reported performance is specific to the dataset and evaluation methodology used in this research project and should not be interpreted as clinical validation.

<br>

## Research Significance

This work investigates the use of **speech-based acoustic features and machine learning for Ayurvedic Prakriti classification**.

The project demonstrates how signal processing, feature engineering, and subject-level machine learning evaluation can be combined to investigate computational approaches to traditional health assessment.

The research also highlights the importance of appropriate validation strategies when working with multiple observations from the same individual.

<br>

## Technologies & Tools

- **Python**
- **Machine Learning**
- **Random Forest**
- **Scikit-learn**
- **Exploratory Data Analysis (EDA)**
- **eGeMAPS**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**

<br>

## Installation & Usage
```bash
git clone https://github.com/Jiyaapatil35/Speech-Based-Ayurvedic-Prakriti-Prediction.git
cd speech-based-ayurvedic-prakriti-prediction
pip install -r requirements.txt
````
<br>

## Research Context

This project was undertaken during a **Research Internship at IIIT Dharwad** and involved collaborative work in speech processing and machine learning.

The project provided practical experience in:

- Research-oriented machine learning
- Speech signal analysis
- Acoustic feature engineering
- Handling subject-level datasets
- Preventing data leakage
- Model evaluation and comparison
- Applied AI/ML research

<br>

## Disclaimer

This project was developed for **academic and research purposes**.

It is an experimental machine learning research project and has **not been clinically validated**. It should not be used as a substitute for professional Ayurvedic consultation, medical diagnosis, or treatment.
