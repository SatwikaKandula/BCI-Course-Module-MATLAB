# BCI Course Module — MATLAB Implementation

## Overview
This module is developed as part of an Advanced BCI Course at UMBC.
Students learn to classify brain signals using EEG data and control 
a virtual robot using motor imagery — implemented entirely in MATLAB.

## Tracks
- **400 Track** — Foundations: Load, visualize, filter EEG, train SVM
- **600 Track** — Advanced: CSP features, EEGNet, CNN classifiers

## Dataset
PhysioNet EEG Motor Movement/Imagery Dataset
- 10 subjects (S001–S010)
- 3 runs each (R03, R07, R11)
- 64 channels, 160 Hz sampling rate
- Classes: T0 = Rest, T1 = Left fist, T2 = Right fist

https://physionet.org/content/eegmmidb/1.0.0/

## Tools
- MATLAB R2023b
- EEGLAB v2026.0.0
- Statistics and Machine Learning Toolbox
- Signal Processing Toolbox

## Live Scripts
- 01_load_and_visualize.mlx — Load and plot raw EEG signals
- 02_epoch_extraction.mlx — Extract and combine epochs across subjects
- 03_svm_classifier.mlx — Train SVM and generate robot commands

## Results
- SVM Accuracy: 51.8%
- Confidence threshold command distribution:
  - LEFT: 32.3%
  - RIGHT: 29.3%
  - REST: 38.3%

## Robot Control (Coming Soon)
- LEFT prediction → raise robot left arm
- RIGHT prediction → raise robot right arm
- REST prediction → robot returns to neutral

## GitHub
- Python version: https://github.com/SatwikaKandula/BCI-Course-Module
- MATLAB version: https://github.com/SatwikaKandula/BCI-Course-Module-MATLAB

## Progress
- [x] Project setup
- [x] Load and visualize EEG data
- [x] Band-pass filtering (8-30 Hz)
- [x] Epoch extraction (T0, T1, T2)
- [x] Combine 10 subjects x 3 runs = 900 epochs
- [x] SVM classifier — 51.8% accuracy
- [x] Confidence threshold approach
- [x] 2D MATLAB robot animation using classifier output
- [ ] VRsink virtual robot integration [If toolbox support is available]
