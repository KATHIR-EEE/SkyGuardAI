# SkyGuard AI — System Architecture

## End-to-End Flow

Sensors → ESP32 → MQTT → Raspberry Pi → AI/Analytics → Hybrid Decision Engine → Explanation Layer → Streamlit Dashboard

## Component Roles

- **Sensors:** Measure temperature, humidity and atmospheric pressure.
- **ESP32:** Collects sensor readings and publishes them through MQTT.
- **MQTT:** Provides lightweight publish/subscribe communication.
- **Raspberry Pi:** Performs edge-side processing, model inference and dashboard hosting.
- **Isolation Forest:** Detects unusual multi-feature observations.
- **Z-score analysis:** Measures deviation from the normal sensor baseline.
- **Weather API:** Provides an independent external reference.
- **Hybrid Decision Engine:** Combines AI, statistical and reference signals.
- **Explanation Layer:** Identifies the parameter contributing most to the detected deviation.
- **Streamlit Dashboard:** Presents real-time status, trends, anomalies and explanations.
