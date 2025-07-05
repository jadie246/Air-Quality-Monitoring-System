# 🌫️ Air Quality Monitoring System Simulation in C

This project simulates a basic **air quality control system** using C language. It mimics real sensors by generating random values for:

- **PM2.5** (particulate matter ≤ 2.5µm)
- **Temperature**
- **CO2 levels**

The system provides **real-time warnings** if any value exceeds a defined threshold and **logs the data to a `.txt` file**.

---

## 📌 Features

- 🔄 Periodic simulation of environmental data
- 📊 Simulated sensors:
  - PM2.5 in µg/m³
  - Temperature in °C
  - CO2 in ppm
- ⚠️ Alerts for abnormal air conditions
- 📝 Logging to `air_quality_log.txt` with timestamps and alert flags

---

## 🧠 How It Works

- Random values are generated using `rand()` and normalized to float range with:
  ```c
  float value = min + ((float)rand() / RAND_MAX) * (max - min);
