# SkyGuard AI

Intelligent real-time anomaly detection system for Automatic Weather Stations.

SkyGuard AI combines Isolation Forest, Z-score analysis, external weather-reference comparison, a hybrid decision engine, and a Streamlit dashboard for interpretable sensor monitoring.

## Architecture

Sensors → ESP32 → MQTT → Raspberry Pi → AI/Analytics → Hybrid Decision Engine → Dashboard

## AI Stack

- Isolation Forest — unsupervised anomaly detection
- Z-score — statistical baseline deviation
- Weather API — independent external reference
- Hybrid decision engine — combines detection signals
- Explanation layer — identifies the primary contributing sensor

## Hardware

ESP32, temperature/humidity/pressure sensors, Raspberry Pi, and network connectivity.

## Run

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
streamlit run dashboard.py
```

## Limitations

The current prototype has limited labelled fault data, so detection performance varies by node and anomaly type. External weather data is a reference rather than absolute ground truth.

## Future Scope

Adaptive baselines, larger real-world fault datasets, explicit sensor-disconnect detection, hardware GPS, cloud monitoring, alerts, and expanded multi-station deployment.
