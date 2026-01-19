# Detecting Parkinson’s Disease using Voice Measurements

## 📌 Project Overview
Parkinson's disease is a progressive neurodegenerative disorder that primarily affects movement and causes tremors and stiffness. With an estimated 7 to 10 million people affected worldwide, this chronic condition currently has no cure. Early and accurate diagnosis is critical for managing symptoms and improving the quality of life for patients.

This project focuses on building a machine learning classification model to detect Parkinson's disease by analyzing vocal measurements (speech signals). The goal is to distinguish healthy individuals from those with the disease based on specific characteristics extracted from voice recordings.

## 📊 Dataset Description
The dataset used in this project was created by **Max Little of the University of Oxford**, in collaboration with the National Centre for Voice and Speech.

- **Total Instances**: 195 recordings
- **Total Attributes**: 23 (Voice-related features)
- **Target Variable (`status`)**: 
  - `1`: Parkinson's Disease
  - `0`: Healthy

### Key Vocal Features Analyzed:
- **Fundamental Frequency**: Average (`MDVP:Fo(Hz)`), Max (`MDVP:Fhi(Hz)`), and Min (`MDVP:Flo(Hz)`) frequencies.
- **Jitter**: Variation in fundamental frequency (measures like `MDVP:Jitter(%)`, `MDVP:RAP`, `MDVP:PPQ`).
- **Shimmer**: Variation in amplitude (measures like `MDVP:Shimmer`, `Shimmer:APQ3`, `MDVP:APQ`).
- **Noise-to-Harmonics**: `NHR` and `HNR` ratios.
- **Nonlinear Complexity**: `RPDE` and `D2` (dynamical complexity) and `DFA` (fractal scaling exponent).
- **Frequency Variation**: `spread1`, `spread2`, and `PPE`.

## 🛠️ Project Workflow

### 1. Data Exploration & Preparation
- **Importance**: Before modeling, it is essential to understand the structure and quality of the data. This step ensures there are no missing values and that feature types are appropriate for the algorithm.
- **Outcome**: A clean dataset ready for processing with 23 predictive real-valued attributes.

### 2. Feature Selection (Recursive Feature Elimination - RFE)
- **Importance**: High-dimensional data often contains redundant or irrelevant features. RFE helps in selecting the most impactful features that contribute to the model's accuracy.
- **Outcome**: Identification of the top vocal biomarkers that indicate the presence of Parkinson's.

### 3. Machine Learning Classification
- **Importance**: The project uses a classification approach to automate the diagnosis process.
- **Metrics**: The model's performance is evaluated using **ROC Curves (Receiver Operating Characteristic)** to measure the ability of the classifier to distinguish between the two classes.

## 📈 Key Outcomes
- **Voice as a Biomarker**: The project demonstrates that voice measurements, particularly nonlinear measures like `RPDE` and `D2`, are significant indicators of Parkinson’s disease.
- **Non-Invasive Diagnosis**: This approach provides a non-invasive, cost-effective way to screen for the disease using digital recordings.

## 🚀 Getting Started

### Prerequisites
To run this project, you need the following Python libraries:
```bash
pip install numpy pandas matplotlib seaborn plotly scikit-learn
