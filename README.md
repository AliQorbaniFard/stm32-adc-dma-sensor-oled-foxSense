# 🦊 Fox Sense – STM32 Dual-Channel ADC + DMA Sensor Dashboard

![Thumbnail](https://github.com/user-attachments/assets/62fd0a1e-dc1d-475a-b06a-ac715b3acc0f)


**Fox Sense is a compact embedded system project built around the STM32F1 series microcontroller.
It reads temperature and ambient light using dual ADC channels with DMA and displays real-time data on a 0.96” SSD1306 OLED.**

The UI reacts visually to the environment:

- 🌡 Temperature displayed in Celsius (LM35)
- 💡 Light detected → Bulb icon
- 🌙 Darkness detected → Moon icon

This project demonstrates practical use of ADC + DMA + I2C display control in an efficient embedded design.

---

### ✨ Features

- Dual-channel ADC sampling (LM35 + LDR)
- DMA-based data transfer (low CPU usage)
- Real-time temperature display in °C
- Light/dark detection with icon switching
- SSD1306 OLED interface via I2C
- Clean modular code structure
- Designed for STM32F1 (tested on STM32F100/STM32F103)

---

### 🛠 Hardware Requirements

- STM32F103C8
- LM35 temperature sensor
- LDR + 10kΩ resistor (voltage divider)
- 0.96” SSD1306 OLED (I2C)
- Breadboard + jumper wires
- 3.3V power supply

---

### 🧠 How It Works

1️⃣ Analog Sensing
- Channel 1: LM35 → outputs 10mV per °C
- Channel 2: LDR voltage divider → light intensity

2️⃣ ADC + DMA
- ADC scans both channels continuously.
- DMA transfers conversion results directly to memory.
- CPU remains free for UI and logic tasks.
	​

3️⃣ OLED Interface
- SSD1306 controlled over I2C
- Custom icons stored as monochrome C arrays
- Real-time screen updates

---

### 🚀 Getting Started

1. Open project in STM32CubeIDE
2. Configure clock (typically 8MHz external crystal or internal RC)
3. Build and flash firmware
4. Adjust light or temperature and observe OLED response

---

### 🎬 Demo

Watch the full demonstration on
[Sly Fox Electronics YouTube Channel](https://youtube.com/@slyfoxelectronics?si=nL4AMqBF7UZqJSDj)

---

### 📜 License

MIT License – Free to use and modify.

---

### 💡 Why This Project Matters

This project demonstrates:

- Practical use of DMA in embedded systems
- Multi-channel ADC configuration
- Sensor interfacing
- Embedded UI design
- Clean firmware architecture

Ideal as a portfolio project for embedded engineering roles.
