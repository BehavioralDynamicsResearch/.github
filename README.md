# Uncertainty-Aware Anomaly Detection for Micro-Behavior Analysis

This repository contains the official implementation for the research project **"Uncertainty-Aware Anomaly Detection with Robust Feature Learning for Micro-Behavior Analysis."**

## Project Overview

In real-world video surveillance, AI-driven anomaly detection systems face significant challenges due to inherent data imperfections such as noise, partial occlusion, and low resolution. Traditional models often provide binary classifications (normal/abnormal) without indicating their confidence, leading to high false alarm rates and diminished user trust.

This project proposes a novel framework for **Uncertainty-Aware Anomaly Detection** in micro-behavior analysis. Our method not only identifies anomalous spatio-temporal patterns but also quantifies the **predictive uncertainty** associated with each detection. By explicitly providing confidence measures, our system aims to offer more accurate and reliable insights, reducing the costs associated with ambiguous warnings and enhancing overall AI system trustworthiness.

## Key Features & Contributions

* **Uncertainty Quantification:** Integrates advanced techniques like Monte Carlo Dropout within the anomaly detection model to quantify the uncertainty of its predictions.
* **Self-Supervised Learning (SSL):** Utilizes SSL (specifically, an Autoencoder-based approach) to learn robust behavioral representations from large-scale unlabeled normal video data, crucial for handling complex and subtle human movements without extensive manual labeling.
* **Robust Anomaly Detection:** Aims to effectively identify anomalous micro-behaviors even under noisy and imperfect real-world conditions.
* **Enhanced System Reliability:** By providing uncertainty information, the system enables more informed decision-making, reduces false positives, and increases user trust.
* **Micro-Behavior Analysis:** Focuses on detecting subtle and fine-grained deviations in human actions.

## Pipeline

Our system's core pipeline involves:

1.  **Video Stream Processing:** Input raw video data.
2.  **Object Detection:** YOLOv10n is used to detect `person` objects within each frame.
3.  **Behavioral Feature Extraction:** Bounding box information (position, size, velocity) of detected persons is extracted as features.
4.  **Uncertainty-Aware Anomaly Detection Model (SSL-Autoencoder + MC Dropout):** The extracted features are fed into our trained model to classify behavior as normal or anomalous, along with a quantified uncertainty measure.
5.  **Result Visualization:** Anomaly scores and uncertainty indicators are overlaid on the original video for clear interpretation.

## Contact

Jiwon Kim - c011058@g.hongik.ac.kr
