# CarDash-Ultra_v1
Futuristic ESP32-S3 Car Dashboard with Composite Video Output



# 🚗⚡ CarDash Ultra v2.6
### Futuristic ESP32-S3 Car Dashboard with Composite Video Output

<div align="center">

![ESP32-S3](https://img.shields.io/badge/ESP32--S3-N16R8-blue?style=for-the-badge)
![LVGL](https://img.shields.io/badge/LVGL-v9.x-00E5FF?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active%20Development-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-orange?style=for-the-badge)

### Cyberpunk-inspired dashboard built entirely on ESP32-S3.

Real-time sensors • Composite Video • BLE Integration • Smart Fuel Assistance

</div>

---

# 📖 About

**CarDash Ultra** adalah dashboard mobil futuristik berbasis **ESP32-S3** yang dirancang untuk menampilkan berbagai informasi kendaraan secara real-time melalui layar **AV Composite (NTSC)**.

Berbeda dengan dashboard DIY biasa, CarDash Ultra menggabungkan:

- Tampilan cyberpunk modern.
- Monitoring sensor kendaraan.
- Integrasi BLE dengan smartphone.
- Sistem navigasi otomatis.
- Analisis performa berkendara.
- Sistem peringatan audio cerdas.

Semua berjalan pada satu board:

> **ESP32-S3 N16R8 (16MB Flash + 8MB PSRAM)**

---

# ✨ Features

## 🚀 Real-Time Vehicle Monitoring

### Speedometer
- Hall Effect Wheel Speed Sensor
- Update rate 20Hz
- Low-pass filtering
- Anti-noise ISR
- Trip odometer

---

### Tachometer (RPM)
- Optocoupler isolated input
- RPM warning zone
- Critical RPM detection
- Shift light indicator

---

### Engine Temperature
- DS18B20 sensor
- Overheat warning
- Critical temperature alert

---

### Battery Voltage Monitor
- Real-time voltage reading
- Weak battery detection
- Audio warning

---

### Fuel Monitoring
- Fuel sender support
- Fuel percentage
- Remaining liters
- Estimated driving range
- Fuel consumption calculation

---

### Gear Detection
Supports:

- R
- N
- 1
- 2
- 3
- 4
- 5

Using Hall Effect sensors.

---

### G-Force Meter

Displays acceleration forces from:

```
-2G  ←──── 0 ────→ +2G
```

Calculated from Hall speed delta.

---

### Trip Computer

Displays:

- Current trip distance
- Total odometer
- Engine hours
- Fuel efficiency
- Lap count

---

# 🗺 Smart Fuel Assistant

One of CarDash Ultra's flagship features.

When fuel becomes low:

1. Dashboard detects fuel level.
2. Checks BLE connection.
3. Gets GPS position.
4. Automatically searches:

```
SPBU Pertamina terdekat
```

5. Sends navigation request to smartphone.
6. Opens Google Maps.

No need to manually search for fuel stations.

---

# 🔔 Intelligent Alert System

Passive buzzer with different warning patterns.

| Condition | Pattern |
|----------|----------|
| Low Battery | 1 Long Beep |
| Engine Warning | 2 Medium Beeps |
| Engine Critical | 3 Long Beeps |
| Overspeed | 4 Fast Beeps |
| Critical Fuel | 5 Fast Beeps |

Cooldown system prevents alert spam.

---

# 📈 Speed History Graph

Displays:

- Last 60 seconds speed history.
- Waveform animation.
- Color coded bars.

Color indicators:

🟦 Normal

🟨 Moderate

🟧 Fast

🟥 Overspeed

---

# 📱 BLE Smartphone Integration

Powered by:

## ChronosESP32

Features:

- Notification mirroring
- Weather synchronization
- Clock synchronization
- Navigation data
- Smartphone connectivity status

---

# 🎨 User Interface

Inspired by futuristic vehicle dashboards.

Features:

- Cyberpunk design
- Cyan glow accents
- RPM arc visualization
- Speed centered layout
- Dynamic shift lights
- Animated waveform
- Navigation widgets
- Notification popups
- Night mode dimming

---

# 🛠 Hardware Requirements

## Main Controller

- ESP32-S3 N16R8

---

## Sensors

- DS18B20 Temperature Sensor
- A3144 Hall Effect Sensor (Speed)
- Hall Effect Sensors (Gear)
- GPS Module
- Passive Buzzer
- Fuel Sender
- Optocoupler PC817

---

## Display

- AV Composite Display
- NTSC 720×480

---

# 🔌 GPIO Pinout

| GPIO | Function |
|-------|----------|
| GPIO4 | RPM Input |
| GPIO5 | DS18B20 |
| GPIO6 | Battery Voltage |
| GPIO7 | GPS RX |
| GPIO8 | GPS TX |
| GPIO9 | Fuel Sender |
| GPIO10 | Hall Speed Sensor |
| GPIO11 | Passive Buzzer |
| GPIO21 | Gear 1 |
| GPIO22 | Gear 2 |
| GPIO35 | Gear 3 |
| GPIO36 | Gear 4 |
| GPIO37 | Gear 5 |
| GPIO38 | Reverse Gear |

---

# 📚 Libraries

Required Arduino libraries:

- LVGL v9.x
- LovyanGFX
- ChronosESP32
- TinyGPS++
- OneWire
- DallasTemperature
- Preferences

---

# ⚙ Arduino IDE Settings

| Setting | Value |
|---------|---------|
| Board | ESP32S3 Dev Module |
| CPU Frequency | 240 MHz |
| Flash Size | 16 MB |
| PSRAM | OPI PSRAM |
| USB Mode | CDC and JTAG |
| Partition | Huge APP |
| Flash Mode | QIO |

---

# 📸 Screenshots

Place screenshots inside:

```
docs/
```

Example:

```
docs/dashboard-ui.jpg
docs/wiring-diagram.png
docs/speed-graph.jpg
```

---

# 🏁 Project Goals

CarDash Ultra was created to explore how far an ESP32-S3 can be pushed beyond traditional IoT applications.

The project aims to combine:

- Automotive telemetry
- Embedded systems
- Real-time graphics
- Smartphone integration
- Futuristic interface design

into a single open-source platform.

---

# ⚠ Disclaimer

This project is intended for educational and experimental purposes.

It is **NOT certified for safety-critical automotive applications**.

Use at your own risk.

Always verify sensor readings before relying on them while driving.

---

# 🤝 Contributing

Contributions are welcome.

You can help by:

- Improving UI performance.
- Adding CAN Bus support.
- Supporting OBD-II adapters.
- Optimizing composite rendering.
- Reporting bugs.
- Suggesting new features.

---

# 🗺 Future Roadmap

- [ ] OBD-II Integration
- [ ] CAN Bus Support
- [ ] Tire Pressure Monitoring
- [ ] Bluetooth Music Widget
- [ ] Voice Assistant
- [ ] Reverse Camera Overlay
- [ ] AI Driving Assistant
- [ ] Theme Customization
- [ ] OTA Updates

---

# ⭐ Support This Project

If you like this project:

⭐ Star this repository

🍴 Fork it

🐛 Report issues

💡 Suggest ideas

---

<div align="center">

## Built with ❤️, caffeine, and countless debugging sessions.

### CarDash Ultra v2.6
#### "Turning an ESP32 into a futuristic driving experience."

</div>