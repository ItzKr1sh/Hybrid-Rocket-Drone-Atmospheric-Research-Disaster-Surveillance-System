🚀 KrxshLabs – Smart Telemetry & Visual Intelligence System

> “Turning rockets, drones, and disasters into data, evidence, and life-saving intelligence.”








---

📌 Overview

KrxshLabs is a low-cost, high-impact telemetry + visual intelligence platform built on ESP32, ESP32-CAM, and sensors (BMP280, BMP180, MPU6050, GPS, DHT11, EEPROM, NRF24L01).

It was designed as a model rocket black-box + rescue drone system but scales to search & rescue, disaster response, precision agriculture, wildfire detection, and education kits.

This project fuses:

📡 10 Hz Telemetry Logging (altitude, acceleration, gyro, GPS, environment)

🎥 Geotagged ESP32-CAM Visual Evidence

🛰 3D Visualization Website (KrxshLabs Dashboard)

🛠 Scalable Architecture (single rocket, drone fleets, classroom kits)



---

🎯 Objectives / Aims

Build a real-time rocket telemetry recorder (black box for DIY launches).

Provide synchronized video + sensor data for proof, recovery, and analysis.

Extend the same hardware to rescue drones, wildfire mapping, precision farming, and infrastructure inspection.

Demonstrate a low-cost, replicable kit (<₹2000 per node) deployable in classrooms and disaster zones.



---

🔬 Scientific Principles

Newton’s Laws of Motion → Rocket thrust, drag, free-fall.

Aerodynamics → Lift/drag coefficients, apogee detection.

Barometric Pressure & Temperature → Altitude & weather mapping.

IMU Fusion (Accelerometer + Gyro) → Orientation & stability tracking.

Wireless Communication → ESP32 Wi-Fi / NRF24 telemetry streaming.

Computer Vision (TinyML on ESP32-CAM) → Smoke/fire/person detection.



---

⚙️ Hardware Used

ESP32 (Airborne Unit + Ground Unit)

ESP32-CAM (downward/forward camera)

BMP280 / BMP180 (pressure + temperature for altitude)

MPU6050 (accelerometer + gyroscope)

NEO-6M GPS module

DHT11 (temperature + humidity)

EEPROM (persistent storage)

NRF24L01 (wireless telemetry)

LiPo Battery (3.7V, 2000–5000 mAh)

3D-printed or PVC rocket body / drone platform



---

🏗 Construction & Working

1. Airborne Unit (Rocket/Drone)

Logs all sensors @10 Hz (JSON format).

Records video with ESP32-CAM, timestamps aligned to telemetry.

Stores to SD + transmits packets to Ground Unit.

Detects apogee, free-fall, and impact via sensor fusion.



2. Ground Unit

ESP32 base station receives telemetry via NRF24/Wi-Fi.

Saves raw JSON log for analysis.

Optionally relays to KrxshLabs Dashboard for visualization.



3. Visualization Website (KrxshLabs Dashboard)

Upload JSON log → interactive 3D flight path on map.

Overlays camera frames with telemetry (altitude, speed, acceleration).

“Play” button simulates flight in sync with video.

Apple-style UI → minimal, polished, Gen-Z friendly.





---

📊 Example Data Log (JSON, 0.1s resolution)

{
  "timestamp": 1684963203000,
  "accelX": 2.0,
  "accelY": 0.1,
  "accelZ": 20.0,
  "gyroX": 0.07,
  "gyroY": 0.06,
  "gyroZ": 0.02,
  "temperature": 32.6,
  "humidity": 77.0,
  "latitude": 20.238480,
  "longitude": 72.907800,
  "altitude": 320.0,
  "speed": 16.0,
  "battery": 11.7,
  "status": "Apogee"
}


---

🔥 Real-Life Applications

🛟 Search & Rescue → Flood/earthquake survivors located via GPS + video.

🌋 Disaster Response → Glacier bursts, bridge/train crashes → live situational awareness.

🌾 Precision Agriculture → Crop health mapping, irrigation savings 10–25%.

🔥 Wildfire Detection → TinyML smoke detection with <200 ms inference.

🏗 Infrastructure Inspection → Pipelines, bridges, rooftops → 60% inspection time saved.

🚀 Rocketry Education → Affordable black-box kits for CBSE schools.



---

✅ Advantages

Ultra low-cost (<₹2000 per node).

Scalable from single rocket to drone fleet.

Replicable with common modules (ESP32, GPS, baro, camera).

Multi-domain: education, rescue, agriculture, disaster.



---

⚠️ Limitations

Wi-Fi / NRF24L01 range limited (~50–300 m).

Camera resolution limited to 640×480 for real-time streaming.

Requires clear weather for GPS & camera reliability.



---

🚀 Future Scope

Add LoRa / LTE gateways for long-range telemetry.

Integrate thermal camera for night rescues & fire hotspots.

Deploy AI dashboards for automated alerting.

Scale into mass-produced CBSE kits & disaster agency nodes.



---

📌 Conclusion

KrxshLabs demonstrates how affordable open-source hardware can transform from a rocket black box into a national disaster-response tool.

From 2018 Kerala Floods to 2023 Odisha Train Crash, this system could’ve saved lives by pairing geotagged visual evidence with millisecond-accurate telemetry.

It’s practical, scalable, and future-ready — built in India, for India, but deployable worldwide.


---

📚 References

NDRF Disaster Response Reports (2018–2023)

CBSE Science Exhibition Guidelines

Espressif ESP32 + ESP32-CAM Documentation

BMP280, MPU6050, NEO-6M, NRF24L01 datasheets

NASA Model Rocketry Guides

