# Propagation and Mitigation of Propaganda in Social Networks

## Overview
This project presents an integrated system for detecting propaganda in textual content and analyzing its propagation across social networks. It combines Natural Language Processing (NLP), Machine Learning, Deep Learning, and Social Network Analysis (SNA) to study both classification and diffusion behavior in a unified framework.

The system is designed for academic and research purposes to understand how propaganda spreads and how it can be controlled using network-based interventions.

---

## Problem Statement
Online social networks enable rapid dissemination of information, including propaganda and misleading content. While existing approaches focus primarily on detecting such content, they often do not model how it spreads through networks or identify structural factors influencing its propagation.

This project addresses this gap by combining:
- Text-based propaganda detection
- Network-based propagation simulation
- Mitigation strategies for controlling spread

---

## Dataset
- Language: Originally Hindi, translated to English
- Domain: Social media and news-style textual content
- Preprocessing steps:
  - Translation
  - Removal of null and duplicate entries
  - Text normalization
  - Tokenization and cleaning

Final dataset size:
- Total samples: **2661**
- Propaganda: **1352**
- Non-propaganda: **1309**

---

## Methodology

### 1. Text Preprocessing
- Lowercasing
- Noise removal
- Tokenization
- Cleaning and normalization

### 2. Feature Extraction
- TF-IDF Vectorization
- Transformer-based embeddings

### 3. Classification Models
- Logistic Regression (baseline model)
- BERT (context-aware deep learning model)
- RoBERTa (optimized transformer model)

### 4. Ensemble Approach
A soft voting ensemble combines predictions from all models to improve stability and overall performance.

---

## Network Simulation

### Graph Model
- Barabási–Albert (BA) scale-free network
- Nodes represent users
- Edges represent social connections

### Propagation Model
- SI (Susceptible–Infected) model
  - Susceptible: unaware users
  - Infected: users spreading propaganda

### Key Network Analysis Metrics
- Degree Centrality (identifies hubs)
- Betweenness Centrality (identifies bridges)

---

## Mitigation Strategies
The system evaluates the impact of interventions such as:
- Removal of hub nodes (highly connected users)
- Removal of bridge nodes (connectors between communities)
- Reduction of infection probability (β)

These strategies help analyze how propagation can be controlled or reduced.

---

## System Architecture

Input Text  
→ Preprocessing  
→ Feature Extraction (TF-IDF + Transformers)  
→ Classification (LR, BERT, RoBERTa)  
→ Ensemble Prediction  
→ SI Propagation Simulation (if propaganda detected)  
→ Network Visualization  
→ Mitigation Analysis  

---

## Technologies Used
- Python
- Scikit-learn
- PyTorch
- Transformers (HuggingFace)
- NetworkX
- PyVis
- Pandas
- NumPy

---

## Features
- Propaganda classification using multiple ML/DL models
- Ensemble-based prediction system
- SI-based propagation simulation
- Social network construction using BA model
- Identification of influential nodes
- Mitigation strategy simulation
- Interactive network visualization
- Explainability through word importance analysis (XAI)

---

## Results Summary
- Transformer models (BERT and RoBERTa) improved contextual understanding of text compared to traditional methods.
- The ensemble model provided more stable and balanced performance than individual classifiers.
- The SI model effectively demonstrated propagation dynamics across a scale-free network.
- Hub nodes significantly accelerated propagation, while bridge nodes enabled cross-community spread.
- Mitigation strategies such as hub/bridge removal and reduction of infection probability reduced overall propagation significantly.
- Visualization using PyVis helped in understanding propagation behavior dynamically.

---

## Limitations
- Dataset is limited in diversity and size
- SI model does not include recovery or immunity states
- Synthetic network may not fully represent real-world social platforms
- System is not designed for real-time social media streaming
- Computational cost increases with larger networks and transformer models

---

## Future Scope
- Integration of real-time social media data
- Use of advanced diffusion models (SIR, SIS, opinion dynamics)
- Deployment of lightweight transformer models for efficiency
- Scalability improvements using GPU/parallel processing
- Enhanced explainability and interpretability techniques
- Multi-source and bot-driven propagation modeling

---

## Conclusion
This project provides a unified framework for studying propaganda detection and its propagation in social networks. By combining machine learning, deep learning, and network analysis, it enables both classification of textual content and simulation of information spread. The system helps in understanding structural and behavioral aspects of propagation and provides insights into effective mitigation strategies.

---
## UI Screenshots
<img width="1919" height="868" alt="image" src="https://github.com/user-attachments/assets/88c7953c-52cb-49d6-a723-552900d64dd9" />
<img width="1538" height="736" alt="image" src="https://github.com/user-attachments/assets/8a4c6e29-b796-493c-991e-ed8f1abe33b7" />
<img width="1553" height="758" alt="image" src="https://github.com/user-attachments/assets/c3ce07bd-740f-4b71-b9bb-1699e0660c85" />



## Note
This project is developed for academic and research purposes only and does not involve real-time monitoring or user tracking.
