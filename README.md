# 🚗Car_black_box

A system designed to log vehicle data including time, speed, and gear events. This project demonstrates how to interface a microcontroller with various peripherals using industry-standard protocols.

### ⚙️ How it Works
1. **Real-Time Tracking:** Uses a DS1307 RTC to display the current time on a CLCD.
2. **Speed Simulation:** Uses an ADC with a potentiometer to simulate changing vehicle speed.
3. **Data Logging:** Records events (Gear shifts/Collisions) and stores them in an external EEPROM via I2C.
4. **Security:** A password-protected menu allows users to view or clear the stored logs.

### 🛠️ Tech Stack
* **Language:** Embedded C
* **Microcontroller:** PIC16F877A
* **Protocols:** I2C, UART
* **Components:** DS1307 RTC, 24C02 EEPROM, 16x2 CLCD, Digital Keypad, ADC

### 📂 File Structure
* `black_box.c`: Main logic for logging and menu navigation.
* `i2c.c / ds1307.c`: Communication drivers for the clock and memory.
* `adc.c`: Driver for speed data acquisition.
* `clcd.c`: Driver for the display interface.

### 💡 Key Learnings
* Mastering **I2C communication** for external memory and RTC.
* Implementing a **Password Authentication** system in an embedded environment.
* Handling **Data Persistence** to ensure logs are saved even if power is lost.
