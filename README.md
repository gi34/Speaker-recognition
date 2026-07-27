# Unlabelled Speaker Recognition
This repository contains the proposed solutions for unsupervised clustering speaker recognition task. This project tackle the clustering of over 200 unlabelled recordings to distinguish between speakers using unsupervised clustering algorithm.

---
# Dataset: CMU ARCTIC
This project use Speaker Recognition - CMU ARCTIC dataset from Kaggle.

- source: https://www.kaggle.com/datasets/mrgabrielblins/speaker-recognition-cmu-arctic
- Content: The dataset includes 12466 recordings with ground truth speaker labels.
- Format: The recordings are provided in `.wav` format at 16kHz sample rate. The data is organized into `train/` and `test/` folders with corresponding CSV files that map file paths to speaker labels and transcriptions

> **Note:** The original dataset is labelled for supervised tasks, this project treat it as **unlabelled** to simulate real-world scenario. Unsupervised learning algorithm is used in this case, and the speaker labels are merely for assessing the clustering performance. 

---
# Overview
This repository proposed solutions for clustering over 200 recordings to 200 speakers, and identifying the cluster of a new recording.
The four stages:

1. **Data Preprocessing**: Resampling, noise reduction, voice activity detection (VAD) and RMS normalization.
2. **Feature Extraction**: Generate speaker embeddings using pre-trained model (x-vector and ECAPA-TDNN). Visualise the embeddings use PCA and t-SNE.
3. **Clustering Algorithm**: Three algorithms are proposed: K-Means, Agglomerative Hierarchy Clustering (AHC) and Spectral Clustering. Group the recordings into clusters by using the extracted speaker embeddings.
4. **Evaluation**: Evaluate the clustering performance using internal evaluation metrics (Silhouette Score, Davies-Bouldin Index (DBI) and Calinski-Harabasz Index (CHI)), visual inspection (PCA and t-SNE) and human listening.

---
# Report
The pdf provide a detailed discussion of:
- Data Exploration and Analysis
- Proposed solution and rationale 
- Implementation Strategy: Data Preprocessing, Feature Extraction Techniques, unsupervised learning algorithms and evaluation strategy without ground truth labels.
- Challenges and Considerations: Potential challenges and assumptions on the recordings.

---
# Repository Structure
```
├── README.md
├── Exploring Unlabelled Speaker Recognition.pdf   # Detailed report
├── Speaker_recognition.ipynb                      # Jupyter Notebook with code exploration
```
---
# Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/gi34/Speaker-recognition.git
cd Speaker-recognition
```

### 2. Open the Notebook
The notebook is designed to run in Google Colab or locally with Hyputer Notebook.
- Google Colab: Upload Speaker_recognition.ipynb to Colab and run the cells
- Local: RUn jyputer notebook Speaker_recognition.ipynb in your terminal
