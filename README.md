# Deep Learning-Based Indian Sign Language Recognition using Landmark Sequences

![Python](https://img.shields.io/badge/Python-3.10-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.x-red)
![MediaPipe](https://img.shields.io/badge/MediaPipe-Holistic-green)
![Status](https://img.shields.io/badge/Status-Research_in_Progress-orange)

> A deep learning framework for recognizing Indian Sign Language (ISL) gestures from MediaPipe landmark sequences. This project investigates multiple temporal deep learning architectures, including LSTM, BiLSTM, GRU, BiGRU, and Temporal Convolutional Networks (TCN), for robust gesture recognition.

---

# Abstract

Indian Sign Language (ISL) serves as an essential means of communication for the deaf and hard-of-hearing community. This project aims to develop an automated ISL recognition system using skeletal landmark sequences extracted through MediaPipe Holistic.

Rather than processing raw video frames, the system utilizes landmark-based representations to efficiently capture spatial and temporal information. Multiple deep learning architectures are being investigated under identical preprocessing conditions to evaluate their effectiveness for ISL recognition. Current experimental results indicate that the Temporal Convolutional Network (TCN) achieves the strongest performance among the evaluated models.

---

# Objectives

- Develop an automated Indian Sign Language recognition system.
- Extract skeletal landmarks using MediaPipe Holistic.
- Compare multiple deep learning architectures for sequence classification.
- Improve model generalization using preprocessing and augmentation techniques.
- Identify the most suitable architecture based on comprehensive evaluation metrics.

---

# Key Features

- MediaPipe Holistic landmark extraction
- Landmark-based temporal sequence modeling
- Comparative analysis of LSTM, BiLSTM, GRU, BiGRU, and TCN
- Coordinate-level data augmentation
- Layer Normalization and Label Smoothing
- Comprehensive evaluation using multiple performance metrics
- Structured research documentation and experiment tracking

---

# Current Results

| Metric | Best Current Model (TCN) |
|---------|-------------------------:|
| Test Accuracy | **90.86%** |
| Test Macro F1-Score | **90.06%** |
| Validation Macro F1-Score | **90.11%** |

> **Note:** These results represent the best performance obtained during the current stage of experimentation. Further optimization and evaluation are ongoing.

---

# Dataset

The project utilizes a video-based Indian Sign Language dataset containing isolated gesture samples.

### Data Processing Pipeline

- Video collection
- MediaPipe Holistic landmark extraction
- Wrist-relative coordinate normalization
- Feature scaling
- Coordinate-level data augmentation
- Train–Validation–Test split

### Dataset Characteristics

- **129 Gesture Classes**
- **30 Frames per Sequence**
- **126 Features per Frame**

---

# Methodology

```text
Input Videos
      │
      ▼
MediaPipe Holistic
      │
      ▼
Landmark Extraction
      │
      ▼
Coordinate Normalization
      │
      ▼
Data Augmentation
      │
      ▼
Model Training
      │
      ▼
Performance Evaluation
      │
      ▼
Gesture Prediction
```

---

# Repository Structure

```text
.
├── docs/
│   ├── architecture/
│   ├── data_processing/
│   ├── experiments/
│   ├── literature_review/
│   ├── meeting_notes/
│   ├── project_progress/
│   └── results/
│
├── notebooks/
├── src/
├── models/
├── requirements.txt
└── README.md
```

---

# Technology Stack

- Python
- PyTorch
- MediaPipe Holistic
- OpenCV
- NumPy
- Pandas
- Scikit-learn
- Matplotlib

---

# Documentation

Detailed documentation for each stage of the project is available below:

- 📖 [Literature Review](docs/literature_review/)
- 📝 [Meeting Notes](docs/meeting_notes/)
- 📂 [Data Processing](docs/data_processing/)
- 🏗️ [Architecture](docs/architecture/)
- 🧪 [Experiments](docs/experiments/)
- 📊 [Results](docs/results/)
- 📅 [Project Progress](docs/project_progress/)

---

# Project Status

🚧 **Research in Progress**

This project is currently under active development as part of an undergraduate research initiative. Model optimization, experimental validation, and the accompanying research paper are actively being refined.

---

# Future Work

- Finalize the TCN architecture and complete experimental validation.
- Expand the dataset with additional ISL gesture classes.
- Investigate Transformer-based sequence models.
- Develop a real-time ISL recognition system.
- Extend the framework for continuous sentence-level sign language recognition.

---

# Team

- **Muskan**
- **Muskan Sah**
- **Nancy Shaw**

---

# Supervisor

**Dr. Shweta Jindal**  
Assistant Professor  
Department of Artificial Intelligence & Machine Learning  
Indira Gandhi Delhi Technical University for Women (IGDTUW)

---

# Acknowledgements

We sincerely thank **Dr. Shweta Jindal** for her valuable guidance, continuous support, and constructive feedback throughout this research project.

We also acknowledge the developers of **MediaPipe** and the publicly available **Indian Sign Language datasets** that supported this work.

---

# References

- MediaPipe Holistic
- PyTorch
- OpenCV
- Scikit-learn
- Research papers reviewed during the literature survey
