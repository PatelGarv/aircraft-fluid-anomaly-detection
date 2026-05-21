# ✈️ Aircraft Fluid Health Monitoring — Anomaly Detection

![Python](https://img.shields.io/badge/Python-3.11-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.4-orange)
![License](https://img.shields.io/badge/License-MIT-green)

## Overview
An unsupervised ensemble machine learning system that monitors aircraft
hydraulic and fuel sensor data in real-time to detect anomalies before
they escalate into failures.

## Problem Statement
Aircraft fluid system failures are a leading cause of in-flight incidents.
Early detection using sensor telemetry can prevent costly unscheduled
maintenance and improve safety margins.

## Approach
| Model | Type | Role |
|---|---|---|
| Isolation Forest | Tree-based | Primary anomaly scorer |
| One-Class SVM | Kernel-based | Secondary detector |
| KDE | Statistical | Fuel-flow distribution check |
| **Ensemble (majority vote)** | **Combined** | **Final prediction** |

## Results
| Metric | Value |
|---|---|
| Precision | 2% |
| Recall | 2% |
| Overall F1 Score | 92% |

## Key Features
- Rolling window feature engineering (mean, std, lag, delta)
- SHAP explainability for individual anomaly diagnosis
- 3-tier alert system: NORMAL → ADVISORY → WARNING
- Visual dashboard with real-time severity scoring

## Setup
```bash
git clone https://github.com/yourusername/aircraft-fluid-anomaly-detection
cd aircraft-fluid-anomaly-detection
pip install -r requirements.txt
jupyter notebook notebook/aircraft_anomaly_detection.ipynb
```

## Project Structure
...

## Screenshots
![Dashboard](outputs/dashboard.jpg)
