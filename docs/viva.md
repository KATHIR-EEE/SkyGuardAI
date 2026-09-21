# SkyGuard AI — Viva Quick Reference

## What is the project?
SkyGuard AI is an intelligent real-time anomaly detection system for Automatic Weather Station sensors.

## Why Isolation Forest?
It is an unsupervised anomaly-detection algorithm, so the prototype does not require a large labelled fault dataset.

## Why Z-score?
It quantifies how far a reading deviates from its normal baseline in standard-deviation units.

## Why Weather API?
It provides an independent external reference. It is not treated as absolute ground truth because weather observations can differ spatially and temporally.

## Why hybrid detection?
AI, statistical analysis and external reference comparison provide different signals that can be combined for more informative monitoring.

## Raspberry Pi role
The Raspberry Pi acts as the edge-processing node, running analytics/model inference and the monitoring dashboard.

## Explainability
The explanation layer uses baseline deviation to identify the sensor parameter contributing most to the detected deviation.

## Current limitation
The prototype has limited real labelled fault data, so performance varies across nodes and anomaly types. More real-world fault data, calibration and adaptive baselines are planned.
