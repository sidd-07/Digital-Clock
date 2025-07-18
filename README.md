# ⏰ Digital Alarm Clock using 8051 Microcontroller
> "Because waking up late shouldn't be a hardware problem."
---
## 📌 Project Overview
This project is a **Digital Alarm Clock** built using the **AT89C52 (8051)** microcontroller. It features:
- ⌨️ **4x3 Keypad** input for setting time and alarms  
- 📟 **16x2 LCD** display to show current time and alarm status  
- 🔔 **Buzzer** alert when alarm triggers  
- 🕒 Real-time clock simulation using **Timer 0**
Designed as a **simple embedded systems project**, this serves as a beginner-friendly dive into **8051 microcontroller programming**, **LCD interfacing**, **keypad scanning**, and **GPIO control**.

---
## 🎯 Features

- ✅ Set current time (Hours:Minutes)
- ✅ Set alarm time via keypad
- ✅ Real-time clock with second updates
- ✅ Buzzer rings when time matches alarm
- ✅ LCD displays current time and alarm messages

---
## 🔧 Hardware Requirements

- AT89C52 / 8051 Microcontroller  
- 16x2 LCD  
- 4x3 Matrix Keypad  
- Buzzer  
- Crystal Oscillator (typically 11.0592 MHz)  
- Capacitors & Resistors for timing and pull-up  
- Breadboard / PCB and power supply

---
## 💡 How It Works
1. **LCD Initialization** – LCD is set in 8-bit mode and ready to display messages.
2. **User Time Input** – Keypad is used to input hours and minutes.
3. **Alarm Setting** – Alarm time is stored and monitored in real-time.
4. **Timer 0** – Used to simulate 1-second delay (software polling).
5. **Clock Display** – Time is updated and displayed on LCD.
6. **Alarm Trigger** – If real-time matches the alarm, buzzer is activated.

---
## 🧠 Code Highlights (`alarm.c`)

- `lcdcmd()` and `lcddata()` – Low-level LCD control
- `keypad()` and `scankey()` – Keypad scanning and input
- `settime()` – Set the current time
- `checkconditions()` – Alarm time input and logic
- `clockdelay()` – Simulated second-by-second update using Timer 0
- `main()` – Initializes system, sets time, and starts clock

🧾 You can find the full source code in [`alarm.c`](./alarm.c)

---

## 📦 Files Included

| File Name         | Description                          |
|------------------|--------------------------------------|
| `alarm.c`        | Main C code for 8051 microcontroller |
| `alarm.hex`      | Compiled HEX file for flashing       |
| `alarm.Uv2`      | Keil µVision project file            |
| `Digital Clock using 8051 Microcontroller.pdf` | Project report with diagrams and explanation |

---

## 🛠️ To Run the Project

1. Load `alarm.hex` to your AT89C52 using a suitable programmer.
2. Connect the circuit as per the project schematic (see report).
3. Use the keypad to:
   - Set the current time
   - Set the alarm time
4. Watch time update on LCD.
5. Hear the buzzer ring when alarm time is reached!

---

## ⚠️ Limitations & Improvements

### Known Issues:
- Time resets incorrectly if it reaches 13:60:60.
- No debounce handling on keypad input.
- Timer is software-polled (not interrupt-based).

### Future Enhancements:
- Use interrupt-driven Timer 0 for accurate timing.
- Add EEPROM support to save alarm time across resets.
- Include AM/PM format or 24-hour support.
- Add multiple alarms or snooze functionality.

---
## 🧑‍💻 Author
**Siddartha Reddy**  

---
## 📜 License
This project is open-source and free to use under the [MIT License](https://choosealicense.com/licenses/mit/).

---
## ⭐ Show Some ❤️
If you found this project useful or learned something new, consider giving this repo a ⭐ and sharing it with your peers.

