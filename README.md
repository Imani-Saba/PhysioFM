# PhysioFM
PhysioFM, a hybrid generative multimodal physiological foundation model designed to establish Physiological Representation Learning (PRL) as a new paradigm for human-centered AI.

# Hidden Wellness AI: Multimodal Physiological Representation Learning

This repository presents a step-by-step research pipeline for developing a multimodal physiological AI framework using the WESAD dataset. The project begins with classical machine learning baselines and progressively advances toward deep learning, latent physiological representation learning, and a preliminary Hidden Wellness Index (HWI).

## Project Goal

The main goal of this project is to develop an AI framework that can learn hidden physiological states from multimodal wearable signals. Instead of only predicting a binary stress label, the framework aims to learn a latent physiological representation that can support:

- stress classification,
- missing-sensor reconstruction,
- future physiological state prediction,
- continuous wellness estimation,
- privacy-aware and sparse-sensor physiological intelligence.

This project serves as a proof of concept for a broader research direction on physiological foundation models and adaptive wearable AI.

## Dataset

This project uses the publicly available WESAD dataset.

WESAD includes multimodal physiological recordings from 15 subjects under affective states such as baseline and stress. The chest-worn sensor data include:

- ACC_x, ACC_y, ACC_z: accelerometer signals,
- ECG: electrocardiogram,
- EDA: electrodermal activity,
- EMG: electromyography,
- RESP: respiration,
- TEMP: skin temperature.

The raw signals were processed into synchronized 60-second windows sampled at 32 Hz with 30-second overlap.

Final raw-window dataset:

- 15 subjects,
- 883 windows,
- 1920 samples per window,
- 8 physiological channels,
- 570 baseline windows,
- 313 stress windows.

## Repository Structure

```text
Apple_Hidden_Wellness_AI/
│
├── data/
│   ├── raw/
│   │   └── WESAD/
│   └── processed/
│       └── raw_multimodal_windows/
│
├── results/
│   ├── classical ML results
│   ├── CNN results
│   ├── CNN-BiLSTM results
│   └── latent HWI model results
│
├── figures/
│   ├── ROC curves
│   ├── confusion matrices
│   ├── feature importance plots
│   ├── PCA/UMAP visualizations
│   └── HWI distributions
│
├── notebooks/
│   ├── 03_wesad_all_subjects_LOSO_baselines.ipynb
│   ├── 04_wesad_all_subjects_publication_analysis.ipynb
│   ├── 04A_prepare_raw_multimodal_windows.ipynb
│   ├── 05_wesad_raw_multimodal_1dcnn_baseline.ipynb
│   ├── 05B_wesad_raw_multimodal_cnn_bilstm_baseline.ipynb
│   └── 06_wesad_multimodal_latent_state_hidden_wellness_index.ipynb
│
└── README.md
