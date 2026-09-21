# SkyGuard AI — Methodology

## 1. Data Acquisition
Environmental readings are collected from temperature, humidity and pressure sensors through an ESP32.

## 2. Data Transport
The ESP32 publishes readings using MQTT and the Raspberry Pi receives the data for processing.

## 3. AI Anomaly Detection
Isolation Forest is used as an unsupervised anomaly detector, producing a score used by the decision layer.

## 4. Statistical Analysis
Z-score based deviation is calculated against the normal sensor baseline.

## 5. External Reference
Weather API values can be compared with local sensor values. The API is an independent reference, not absolute ground truth, because observations may differ by location, elevation, timing and calibration.

## 6. Hybrid Decision
AI detection, baseline deviation and reference deviation are combined to produce the monitoring status.

## 7. Explainability
A baseline-deviation contribution calculation identifies the primary sensor contributing to the detected deviation. This is a custom explanation layer, not a SHAP implementation.
