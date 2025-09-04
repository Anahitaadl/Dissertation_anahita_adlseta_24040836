# Dissertation_anahita_adlseta_24040836
Enhancing the Robustness of  AI-Based DDoS Detection Systems in 5G Networks  Against Adversarial Attack


📌 Overview

This repository contains the code, datasets, and methodology for the dissertation project:
“Enhancing the Robustness of AI-Based DDoS Detection Systems in 5G Networks Against Adversarial Attack.”

The project evaluates the adversarial vulnerabilities of machine learning models (XGBoost, Random Forest, and MLP) for DDoS detection in 5G contexts, and implements defenses such as adversarial training, preprocessing filters, and explainability-based monitoring (SHAP/LIME).

📂 Repository Structure

final_code_1.ipy → Main Jupyter Notebook for preprocessing, training, adversarial evaluation, and defenses.
https://colab.research.google.com/drive/1LysT2-QM3TaeEXBGGT2molkzb2_ywOc-

20k_dataset_preprocessed.csv → Cleaned dataset (post preprocessing).

20k_dataset_ml_ready.csv → Feature-engineered dataset ready for ML training.

final_balanced_dataset_20k.csv → Stratified 20k balanced dataset used for experiments.

README.md → Project description and usage instructions.

📊 Datasets Used

This project integrates three benchmark IDS datasets to capture diverse DDoS scenarios:

CICIDS-2017 – Canadian Institute for Cybersecurity IDS dataset.
🔗 (https://www.unb.ca/cic/datasets/ids-2017.html?utm_source=chatgpt.com)

CIC-DDoS2019 – High-volume DDoS traffic dataset.
🔗 (https://www.unb.ca/cic/datasets/ddos-2019.html?utm_source=chatgpt.com)

Bot-IoT – IoT-driven DDoS dataset (UNSW Cyber Range Lab).
🔗 (https://research.unsw.edu.au/projects/bot-iot-dataset?utm_source=chatgpt.com)

The working dataset here (20k_dataset_*.csv) is a stratified sample of 20,000 records (19,227 after cleaning), ensuring balanced representation across benign and attack traffic.

⚙️ Methodology

1.Dataset Integration & Preprocessing

-Cleaning, duplicate removal, handling missing values.

-Standardization applied for feature comparability.

2.Model Training

-XGBoost, Random Forest, and MLP trained on 20% test split.

-5-fold stratified cross-validation for stability.

3.Adversarial Attack Framework

-Evasion (Gaussian/Uniform noise, feature permutation).

-Poisoning (label flipping).

-Backdoor triggers.

4.Defense Mechanisms

-Adversarial training.

-Preprocessing filters (outlier clipping, feature squeezing).

-Backdoor detection.

5.Explainability (XAI)

-SHAP and LIME for explanation stability under attack.

📈 Results Summary

Baseline models reached >98% accuracy on clean test data.

Backdoor attacks achieved >90% success across all models.

Adversarial training improved robustness to ~84% while maintaining <5 ms inference latency.

SHAP explanations showed greater stability compared to LIME under adversarial conditions.

🚀 How to Run

Clone the repo:

git clone https://github.com/<your-username>/Dissertation_anahita_adlseta_24040836.git
cd Dissertation_anahita_adlseta_24040836


Open the Jupyter notebook:

jupyter notebook final_code.ipynb


Run preprocessing, training, and adversarial evaluation cells sequentially.

📜 Citation

If you use this work, please cite:

Anahita Adlseta, Enhancing the Robustness of AI-Based DDoS Detection Systems in 5G Networks Against Adversarial Attack, MSc Dissertation, 2025.
