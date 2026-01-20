# Speech-Based Ayurvedic Prakriti Prediction

## Project Overview
This project presents a machine learning–based approach for predicting Ayurvedic Prakriti types — **Vata, Pitta, and Kapha** — using speech signal analysis. The work explores the feasibility of a non-invasive and objective computational method to support traditional Ayurvedic assessment. The study demonstrates the potential of speech-based biomarkers as an assistive tool for objective Prakriti classification.

The research was **conducted at KLE Technological University, Dr. M.S. Sheshgiri College of Engineering and Technology**, in collaboration with **Indian Institute of Information Technology, Dharwad (IIIT Dharwad).**.


> **Academic Research Project | 5th Semester**  
> **Duration:** September 2025 – January 2026  
> **Team Size:** 4 Members  
> **Technologies:** Python, Exploratory Data Analysis (EDA), Machine Learning, Deep Learning  


## Objectives
- Analyze human speech signals for Prakriti classification  
- Extract clinically relevant acoustic features using eGeMAPS
- Develop a reliable machine learning pipeline for Prakriti prediction  
- Ensure subject-level validation and avoid data leakage  

## Methodology
1. **Speech Data Collection**  
   Real-time speech recordings were collected from participants under controlled conditions.

2. **Feature Extraction**  
   Acoustic features were extracted using the extended Geneva Minimalistic Acoustic Parameter Set (eGeMAPS).

3. **Feature Aggregation**  
   Statistical aggregation (mean, standard deviation, minimum, maximum) was performed at the participant level.

4. **Model Training**  
   A Random Forest classifier with balanced class weights was trained on aggregated features.

5. **Evaluation Strategy**  
   - Subject-level train–test split  
   - 5-fold GroupKFold cross-validation 
   - Comprehensive performance metrics  

## Results
The Random Forest model demonstrated strong predictive performance:

| Metric | Value |
|--------|-------|
| Test Accuracy | **95.89%** |
| Balanced Accuracy | **98.21%** |
| Weighted F1-Score | **96.00%** |

The model outperformed neural network–based approaches such as Multi-Layer Perceptron (MLP) and Feed-Forward Neural Network (FNN).

## Installation & Usage
```bash
git clone https://github.com/Jiyaapatil35/Speech-Based-Ayurvedic-Prakriti-Prediction.git
cd speech-based-ayurvedic-prakriti-prediction
pip install -r requirements.txt
````

**Note:** This project is intended for academic and research purposes only. It does not replace professional Ayurvedic consultation or medical advice. Users should not rely solely on this tool for health or treatment decisions.
