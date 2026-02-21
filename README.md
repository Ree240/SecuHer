<p align="center">
  <img src="./img.png" alt="Project Banner" width="100%">
</p>

# SecuHer 🎯

## Basic Details

### Team Name: Malabar Gang

### Team Members
- Member 1:Anusree Satheesh - Adi Shankara Institue of Engineering and Technology
- Member 2: Sandra N - Adi Shankara Institue of Engineering and Technology

### Hosted Project Link
https://github.com/Ree240/SecuHer

### Project Description
SecuHer is a simple, one-tap safety app designed to protect people during travel. It solves the problem of "silent emergencies" by making it incredibly easy to send your exact location and vehicle details to family or friends in seconds.

What it does:
Emergency SOS: Tap one button to instantly send an SMS to up to 3 saved contacts.
Vehicle Tracking: The message includes the Vehicle Number (like the taxi or bus plate) so rescuers know what car to look for.
Live Location: Sends a clickable Google Maps link so your contacts can navigate to you immediately.
Offline Mode: Works via SMS, meaning it works even if you don't have internet or a 4G data plan.

How it works:
You enter your emergency contacts and vehicle number once. If you feel unsafe, you hit the SOS button. SecuHer grabs your GPS coordinates and blasts a message out to everyone you trust—no internet required.

### The Problem statement
In many travel scenarios, existing safety measures are either too slow or fail when most needed. Current solutions face three critical gaps:

Internet Dependency: Most safety apps require high-speed data (4G/5G). In rural areas, basements, or moving vehicles, internet connectivity is often unstable, rendering these apps useless.
Information Gap: A GPS location tells a responder where you are, but in a busy street or highway, they don't know which vehicle you are in. Rescuers often waste "Golden Hour" minutes trying to identify the correct car.
Complex Interfaces: During a panic situation, users cannot navigate through multiple screens or menus to trigger an alert.
SecuHer addresses these issues by providing a one-tap, offline-first solution that instantly communicates both a clickable GPS location and vehicle identification details via standard SMS protocol.

### The Solution
SecuHer is a "one-tap" safety app that ensures help reaches you even without an internet connection.

Offline Alerts: Sends emergency messages via SMS, so it works in areas with zero data/Wi-Fi.
Identification: Includes the Vehicle Number in the alert so rescuers know exactly which car to look for.
Instant Location: Sends a clickable Google Maps link for immediate navigation to your exact spot.
Panic-Ready: Designed with a simple interface so you can call for help in one second.

## Technical Details
SecuHer is built to be lightweight and reliable using the following core tools:

Development Platform: MIT App Inventor (Android).
GPS Tracking: Uses the Location Sensor to grab real-time Latitude and Longitude.
Communication: Uses the SMS/Texting Component to send alerts without needing internet (Offline-First).
Logic: Uses Global Variables to store your contact numbers and vehicle ID while the app is running.

How it works:
Capture: The app gathers your current coordinates from GPS satellites.
Format: It "joins" your vehicle number and coordinates into a clickable Google Maps link.
Blast: It triggers the phone's SMS manager to send that link to all your saved contacts instantly.

### Technologies/Components Used
MIT App Inventor: App building platform.
GPS Sensor: For real-time location tracking.
SMS Component: To send alerts without internet.
Variables: To store contacts and vehicle details.
Google Maps API: To generate clickable location links

**For Software:**
- Languages used: Kawa/scheme,Blockly
- Frameworks used:Mit App Inventor
  - Tools used: Google app engine

**For Hardware:**
- Main components: GPS Module: For coordinate tracking.,GSM Modem: For sending SMS alerts,Processor: Minimum 1.0 GHz,RAM: 512MB or higher.
- Specifications
OS: Android 2.1+ (Android 9.0+ recommended),Storage: ~20MB for APK installation,Network: Active SIM card with SMS plan.

---

## Features

List the key features of your project:
- Feature 1: Emergency SOS: Tap one button to instantly send an SMS to up to 3 saved contacts.
- Feature 2:Vehicle Tracking: The message includes the Vehicle Number (like the taxi or bus plate) so rescuers know what car to look for.
- Feature 3: Live Location: Sends a clickable Google Maps link so your contacts can navigate to you immediately.
- Feature 4:Offline Mode: Works via SMS, meaning it works even if you don't have internet or a 4G data plan.

---

## Implementation
Setup Phase: User inputs emergency mobile numbers and the vehicle registration details into the app.
Location Capture: On clicking the SOS button, the app activates the LocationSensor to fetch real-time GPS coordinates.
Data Processing: The app logic "joins" the vehicle ID and a Google Maps URL into a single string.
Execution: The Texting component automatically loops through the contacts and dispatches the formatted SMS.
Alert Delivery: The receiver gets a text with the vehicle details and a clickable link to navigate directly to the user.
### For Software:

#### Installation
Download Source: git clone https://github.com/your-username/SecuHer.git
Import: Go to ai2.appinventor.mit.edu.
Upload: Click Projects -> Import project (.aia) from my computer.
Select File: Choose SecuHer.aia from your cloned folder.

#### Run
Live Testing: Open the MIT AI2 Companion app on your phone and scan the QR code from the App Inventor browser. This runs your changes in real-time.
Manual Install: Transfer the .apk file to your phone’s internal storage and tap to install/run.
---

## Project Documentation

### For Software:

#### Screenshots (Add at least 3)

![Screenshot1](<img width="957" height="435" alt="Screenshot 2026-02-21 065001" src="https://github.com/user-attachments/assets/33a4d104-64f8-44e6-b699-4f0b32d4f76f" />)1. The User Interface (App Design)
This is what the user sees on their phone screen.
Setup: Fields to type in the vehicle plate number and three emergency phone numbers.
Controls: Buttons to "Start Trip" and "Save" your contact list.
Emergency Trigger: A large red "EMERGENCY SOS" button designed for fast, easy tapping during a panic.


![Screenshot2](![WhatsApp Image 2026-02-21 at 07 45 39](https://github.com/user-attachments/assets/30b11bce-8a6c-44a8-80b8-8a6b5fd7f204))
2. The Logic (Code Blocks)
This is the "brain" that controls the app's actions behind the scenes.
Dual Triggers: The app sends an alert if the SOS button is clicked OR if the phone is shaken (using the Accelerometer).
Auto-Message: It instantly creates a text message combining the Vehicle ID, a Google Maps location link, and the Time.
Direct Sending: It automatically sends this message to all three contacts without needing the user to type anything.

#### Diagrams

**System Architecture:**

![Architecture Diagram](docs/architecture.png)
*Explain your system architecture - components, data flow, tech stack interaction*

**Application Workflow:**

![Workflow]
Workflow:
User Setup: User enters vehicle details and emergency contacts.
Monitoring: User taps "Start Trip" to activate the system.
Emergency Trigger: User either taps the SOS Button or Shakes the phone.
Data Retrieval: App fetches current GPS Coordinates and the current Time.
Alert: App auto-sends an SMS with a Google Maps link and Vehicle ID to all saved contacts.

---
### For Hardware:
Main Components:
Smartphone: Acts as the central processing unit.
GPS Module: (Internal) For real-time location tracking.
GSM Modem: (Internal) For sending offline SMS alerts.
Accelerometer: (Internal) To detect emergency "shaking" gestures.
Build Steps:
Design UI: Created input fields and a panic button in MIT App Inventor.
Program Logic: Used block coding to link the Accelerometer and GPS to the Texting component.
Permission Setup: Configured the app to request SMS and Location access.
Testing: Verified the "Direct Send" feature works even when the phone is offline.

---

#### Installation Guide

**For Android (APK):**
Download the SecuHer.apk.
Enable "Install from Unknown Sources" in Settings > Security.
Install the APK and grant Location and SMS permissions.
Building from Source:
Download the SecuHer.aia file.
Import into MIT App Inventor.
Click Build > App (.apk).

## AI Tools Used (Chatgpt,Gemini)
**Tool Used:** [e.g., GitHub Copilot,MIT App Inverter,ChatGPT, Claude]

---

## License

This project is licensed under the [LICENSE_NAME] License - see the [LICENSE](LICENSE) file for details.

**Common License Options:**
- MIT License (Permissive, widely used)
- Apache 2.0 (Permissive with patent grant)
- GPL v3 (Copyleft, requires derivative works to be open source)

---
