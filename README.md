# SecuHer
A focused emergency alert application built for [Tink-her-hack] 2026.

## 🌟 Core Feature: One-Tap Emergency Alert
The app is designed for speed and reliability in high-stress situations. 

### What it does:
* **Instant SMS Dispatch:** Sends an immediate emergency text to multiple contacts.
* **Vehicle Identification:** Automatically attaches the vehicle registration number (e.g., KL 07 AB 1234) to the message so responders know what car to look for.
* **Live Location Link:** Includes a precise Google Maps URL with current GPS coordinates.
* **Offline Protocol:** Uses SMS rather than internet data to ensure the message goes through even in low-signal areas.

## 🛠️ How it Works
1. **Input:** The user saves emergency contact numbers and the vehicle number.
2. **Action:** Upon clicking the "SOS" button (or shaking the phone), the app compiles all data.
3. **Execution:** The app loops through the saved contacts and sends a pre-formatted emergency SMS.

## 🏗️ Technical Stack
* **Build Tool:** MIT App Inventor
* **Communication:** Android SMS Component
* **Sensors:** GPS LocationSensor & Accelerometer (Shake detection)
