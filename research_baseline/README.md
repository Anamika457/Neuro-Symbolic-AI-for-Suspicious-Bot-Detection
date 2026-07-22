# Research Baseline Implementation

## Overview

This directory contains the implementation of the research paper that serves as the baseline for the main project.

The objective of this implementation is to reproduce the neuro-symbolic intrusion detection framework proposed by the authors and establish a reliable reference for future development and evaluation.

---

## Reference Paper

**Neurosymbolic Learning and Domain Knowledge-Driven Explainable AI for Enhanced IoT Network Attack Detection and Response**

Kalutharage et al.

*Computers & Security*, 2025

---

## Methodology

The implemented framework consists of three primary components.

### Autoencoder-Based Anomaly Detection

An autoencoder is trained using benign network traffic to learn normal network behavior. During inference, reconstruction error is used as an anomaly score, where samples exceeding a learned threshold are classified as anomalous.

### Explainability using Kernel SHAP

Kernel SHAP is applied to anomalous samples to identify the most influential features contributing to each prediction, providing local explanations for detected attacks.

### Knowledge Graph and Symbolic Reasoning

The framework incorporates cybersecurity domain knowledge through a knowledge graph. Symbolic reasoning combines reconstruction errors, feature thresholds, and logical rules to generate interpretable attack explanations and confidence scores.

---

## Dataset

The implementation uses the **USBIDS** dataset.

Preprocessing includes:

- Feature selection
- Handling missing and infinite values
- Min-Max normalization
- Training using benign samples
- Evaluation on both benign and malicious traffic


---

## Results

The implementation successfully reproduces the core methodology presented in the paper and achieves strong anomaly detection performance on the USBIDS dataset.

| Metric | Implementation |
|---------|---------------:|
| Accuracy | **91.28%** |
| ROC-AUC | **0.9979** |
| Attack Precision | **1.00** |
| Attack Recall | **0.91** |
| Attack F1-Score | **0.95** |
| Benign Precision | **0.13** |
| Benign Recall | **0.99** |
| Benign F1-Score | **0.23** |

### Key Observations

- The autoencoder achieved a **ROC-AUC of 0.9979**, demonstrating excellent separation between benign and malicious traffic.
- **15 of the 16 attack files** achieved detection rates above **98.5%**, with **11** exceeding **99.5%**.
- Most false negatives originated from the **Hulk-Evasive** attack variant, which is significantly harder to detect than the remaining attacks.
- The model generated a low false positive rate on benign traffic (~0.96%), making it suitable as an anomaly detector for high-security environments.
- The symbolic reasoning module correctly classified all evaluated explained anomalies, achieving **100% accuracy, precision, recall, and F1-score** on the sampled evaluation set.

---

## Purpose

This implementation establishes the research baseline for the main project. Future work extends these concepts to suspicious social bot detection using temporal graph neural networks, symbolic reasoning, and neuro-symbolic learning.