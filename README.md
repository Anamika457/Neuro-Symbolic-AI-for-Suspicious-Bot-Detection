# Neuro-Symbolic AI for Suspicious Bot Detection

## Overview

The rapid growth of social media platforms has led to an increase in sophisticated automated and coordinated bot accounts capable of spreading misinformation, manipulating online discourse, and evading conventional detection methods. Although recent Graph Neural Network (GNN)-based approaches achieve high detection accuracy, they often function as black-box models, making it difficult to interpret or justify their predictions.

This project aims to develop a **Neuro-Symbolic AI framework** for suspicious bot detection by integrating graph-based deep learning with symbolic reasoning. The proposed framework combines learned user representations with expert-defined logical rules to accurately classify genuine users, suspicious accounts, automated bots, and coordinated bot networks while providing transparent, human-interpretable explanations for every prediction. :contentReference[oaicite:0]{index=0}

The framework leverages user profile information, content characteristics, temporal activity, and interaction patterns to construct dynamic social graphs. Neural learning captures complex behavioral patterns, while symbolic reasoning incorporates domain knowledge to improve explainability, robustness, and adaptability against evolving bot behavior. :contentReference[oaicite:1]{index=1}

---

## Research Foundation

This project is built upon the research paper:

> **Neurosymbolic Learning and Domain Knowledge-Driven Explainable AI for Enhanced IoT Network Attack Detection and Response**  
> Kalutharage et al., *Computers & Security*, 2025

The paper proposes a neuro-symbolic framework for IoT attack detection by combining anomaly detection, explainable AI, and symbolic reasoning. Its implementation serves as the research baseline for this project, providing the foundation upon which the proposed bot detection framework will be developed.

---

## Current Status

The baseline implementation of the reference paper has been successfully reproduced. The implementation includes:

- Autoencoder-based anomaly detection
- Kernel SHAP explainability
- Knowledge graph construction
- Symbolic reasoning for interpretable predictions

The implementation is available in the **`research_baseline/`** directory.

---

## Future Work

The next phase of the project focuses on developing the proposed Neuro-Symbolic AI framework for suspicious bot detection by:

- Constructing temporal social interaction graphs
- Learning user representations using Graph Neural Networks (GNNs) and Temporal Graph Attention Networks (TGAT)
- Developing a symbolic knowledge base and reasoning engine
- Fusing neural predictions with symbolic inference
- Generating interpretable explanations for bot classifications
- Evaluating the framework on benchmark datasets such as Twibot-22, Twibot-20, Cresci-2017, and Botometer. :contentReference[oaicite:2]{index=2}

---

## References

- Kalutharage et al., **Neurosymbolic Learning and Domain Knowledge-Driven Explainable AI for Enhanced IoT Network Attack Detection and Response**, *Computers & Security*, 2025.