EEG Connectivity Analysis for Neurodegenerative Disease Classification

This repository contains the final year research project on EEG preprocessing, connectivity analysis, and deep learning-based classification of neurodegenerative diseases such as Alzheimer’s Disease (AD), Frontotemporal Dementia (FTD), and Healthy Controls (HC).

The project is structured into multiple stages: automation of preprocessing, connectivity computation, statistical analysis, and deep learning graph-based modeling.

📂 Repository Structure
1. Automation (MATLAB)

The Automation.zip folder contains MATLAB scripts to automate the preprocessing of raw EEG data. The following modules are included:

Band_Notch_filters.m → Filtering raw EEG signals (band-pass & notch filters).

noise_covariance.m → Estimation of noise covariance matrices.

ICA_Components.m → Independent Component Analysis for artifact removal.

Power_Spectrum.m → Power spectral density computation.

scout.m → Brain scout definition for source analysis.

Compute_Sources.m → Source reconstruction from sensor-space EEG.

Compute_Head_Model.m → Head model computation.

BEM_Surfaces.m → Boundary Element Method surface modeling.

Coherence_Correct.m → Coherence connectivity computation.

PLV_correct.m → Phase Locking Value (PLV) connectivity computation.

2. Statistical Analysis (MATLAB)

The Statistical_Analysis.zip folder contains MATLAB scripts for statistical testing on connectivity matrices:

Conversion of Coherence and PLV connectivity matrices into CSV format.

t-test analysis on connectivity values between groups (AD, FTD, HC).

Identification of statistically significant connectivity differences.

3. Deep Learning Graph Analysis (Python)
🔹 PLV.ipynb

Loads connectivity CSV files and constructs ε-graphs using cosine similarity.

Applies t-SNE for dimensionality reduction.

Builds graphs using k-NN and mutual k-NN methods.

Implements a Graph Attention Network (GAT)-based Graph Convolutional Network (GCN) model.

Uses 5-fold cross-validation with training, validation, and testing splits.

Generates confusion matrices for performance evaluation.

Investigates the impact of training dataset size on classification accuracy.

🔹 GCN_Final.ipynb

Identifies the top 10 brain region pairs showing significant differences across AD, FTD, and HC groups.

Demonstrates the statistical relevance of connectivity features in classification.

🔹 newcorrected_one.ipynb

Explores how varying the k-value in k-NN graph construction affects GAT model accuracy.

Provides insights into graph topology selection and model robustness.

⚙️ Methodology Overview

EEG Preprocessing → Filtering, artifact removal, head model & source estimation.

Connectivity Computation → Coherence & PLV-based connectivity matrices.

Statistical Analysis → Group-wise statistical testing on connectivity features.

Graph Modeling → Constructing connectivity-based graphs and applying GCN/GAT.

Classification → Multi-class classification between AD, FTD, and HC with performance evaluation.

📊 Key Outcomes

Automated preprocessing pipeline for EEG data.

Statistically validated connectivity features.

Graph-based deep learning models (GCN & GAT) for neurodegenerative disease classification.

Identification of significant brain region pairs differentiating AD, FTD, and HC.

Analysis of dataset size and graph construction parameters on model accuracy.

🚀 Technologies Used

MATLAB → Preprocessing, source modeling, and statistical analysis.

Python (Jupyter Notebooks) → Graph construction, deep learning models, and visualization.

PyTorch Geometric

scikit-learn

NumPy / Pandas

Matplotlib / Seaborn

📌 Citation

If you use this work in your research, please cite appropriately.
