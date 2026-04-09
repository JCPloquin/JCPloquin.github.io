---
title: "HarpEK: The Continuous Gesture Instrument Reaches Maturity"
date: 2025-12-21T14:45:00+01:00
slug: "harpek-design-advances"
draft: false
categories: ["Music", "Technology", "Digital Lutherie"]
tags: ["HarpEK", "ESP32", "Pure Data", "electronic instrument", "OSC", "sensors", "lutherie", "experimental"]
description: "HarpEK project status update: ESP32 platform, ultrasonic harp, pedals and encoders validated. A continuous gestural control instrument designed to overcome MIDI limitations."
image: "/img/harpek_projet.jpg"
---

# HarpEK: The Continuous Gesture Instrument Reaches Maturity

After months of design, testing and adjustments, **HarpEK** reaches a decisive milestone: almost all critical hardware is validated and documented. The instrument takes shape, along with a renewed vision of gestural control in electronic music.

![HarpEK - Enclosure Overview](/img/harpek_projet.png)
*3D modeling of the HarpEK enclosure with ultrasonic sensors, encoders and joystick*

---

## 🎛️ Validated Hardware Architecture

### Platform and Power Supply

The system's core relies on a fully operational **ESP32-S3 DevKitC**:
- Stable programming via Arduino IDE
- USB serial communication at 115200 bps
- Functional OSC-Serial protocol to Pure Data

The 5V / 3.3V power supply has been validated with precision:
- 5V 3A adapter
- AMS1117-3.3V regulator
- Measured voltages: **5.02V** and **3.28V**
- Clean common ground, no parasitic noise

Main switch, power terminal block, and **Chenyang panel-mount USB-C connector** have all been tested and validated both mechanically and electrically.

---

## 🎵 Sensors and Controllers: The Body at the Center of Play

### Ultrasonic Harp (3 × HC-SR04)

HarpEK's flagship feature: **three ultrasonic sensors spaced 80 mm apart** create a continuous gestural detection zone.

**Measured Performance**:
- Stable **Winner-Takes-All** algorithm
- **99% correct detections**
- Latency ≈ **60 ms**
- Useful range: **5–177 cm**
- Distance → pitch mapping already musically exploitable

Each sensor has its **dedicated LED** (GPIO 45/46/47) for immediate visual feedback.

### Expression Pedals (4 × Roland DP-10)

TRS pinout and 5V power supply measured with precision. Voltage dividers **1kΩ / 2kΩ** convert 0–5V signals to usable ADC range (≈0–3.3V), yielding **0–2800 in 12-bit resolution**.

**No crosstalk** between the 4 pedals: each channel remains clean and stable.

### Rotary Encoders (3 × KY-040)

Tested simultaneously in circular mode **0–127 with wrap-around**. Integrated buttons (SW) are reliable, no bounce or crosstalk issues.

### Arcade Joystick (D400X-R4)

Functional version validated: **3 analog axes** (0–4095) + center button. Integration via dividers identical to pedals.

---

## 🧠 Memory Interface and Feedback

### Memory System (4 Gebildet 12mm Buttons)

Eurocard wiring completed and tested. Logic scheme separating **buttons and LEDs**, firmware management planned with **exclusive selection of one active memory** at a time.

Each memory will be able to store a complete configuration of mappings, scales, or Pure Data presets.

---

## 🔧 Electronic and Mechanical Architecture

![HarpEK Internal Architecture](/img/harpek_projet2.png)
*Exploded view: Eurocard, ESP32, connectors and internal wiring*

### Eurocard 100×80 mm

Main board completed with professional quality:
- ESP32 headers soldered
- Power terminal block fixed
- Voltage dividers installed
- Magnifying glass inspection: continuities verified, **no short circuits**

### Complete Connection Table

**85 GPIO connections documented** in a LibreOffice spreadsheet. Each signal, ground, and power supply has been cross-verified. No remaining inconsistencies.

![ESP32-S3 Connection Table](/img/tableau-connexions-harpek.png)
*Comprehensive table of 85 ESP32-S3 GPIO connections*

### Hammond 1455N1602 Enclosure

Complete 3D modeling in **SketchUp**. A4 templates for all 4 faces validated:
- Flush HC-SR04 sensors (front face)
- Encoders, joystick, memory buttons (top face)
- TRS pedal jacks, USB-C, power switch (rear face)
- Internal clearances verified: no mechanical conflicts

---

## 💡 Instrumental Philosophy: Continuous Gesture

HarpEK is not a simple MIDI controller. It's an **instrument designed for continuous gesture**, a response to the limitations of traditional protocols.

### Beyond MIDI

The **OSC-like protocol over USB serial** allows exploitation of the full **12-bit resolution** of sensors, without the 7-bit MIDI constraint. The instrument's language becomes a personal alphabet, mapped in Pure Data to:
- Microtonal scales
- Spectral spaces
- Non-metric rhythmic structures
- 5.1 and 8.1 spatialization

### A 1980s Heritage

HarpEK draws inspiration from **analog joysticks** and **modular synthesis**: the musician shapes continuous flows rather than stacking isolated notes. With the ultrasonic harp, pedals, joystick, and encoders, **the body becomes central again**: every hand or foot movement becomes a sonic trajectory.

### Instrumental Immediacy

The goal: for the musician to think in **gesture and timbre**, not in "parameters" or "messages". HarpEK extends an instrumental tradition into 2025 computer music.

---

## 🚀 Next Steps

With all major technical building blocks validated, the upcoming phases are:
1. **Final assembly** in the Hammond enclosure
2. **Complete calibration** of sensors in real-world situations
3. **Firmware development**: memory management and latency optimization
4. **Dedicated Pure Data patches** for initial musical testing
5. **User documentation** and first test concerts

HarpEK approaches its final form. The instrument is almost ready to play.

---

🎸 *Open hardware project — Designed and documented for the experimental music community.*

