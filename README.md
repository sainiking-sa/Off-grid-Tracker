#  Ai Off-Grid Tracker & Emergency Alert System!

To design and build a fully off-grid, AI-powered smart safety and tracking system that works without internet, SIM, or cloud, using LoRa-based long-range communication and wearable devices, to monitor people in remote and dangerous areas, automatically detect emergency situations, reduce false SOS alerts, and enable fast, reliable rescue operations in places where traditional systems completely fail.

This project is especially suitable for **disaster zones, remote areas, military regions, mines, forests, and off-grid industrial sites**.

---



##  Objectives

* To develop an **internet-independent tracking and communication system** suitable for remote and mountainous regions.

* To ensure the **safety of trekkers and users** by continuously monitoring movement through **pole-based checkpoint tracking**.

* To assist in **disaster management scenarios**, such as floods, landslides, or other emergency situations.

* To provide a reliable **emergency SOS alert mechanism** through wearable devices and tracking poles.

* To enable **faster and more accurate rescue operations** by identifying the **last crossed checkpoint** and transmitting precise location data.

* To design a **scalable, cost-effective, and reliable solution** for outdoor tracking and safety applications.

---

##  Features of Smart Tracking Watch

*  **LoRa-Based Long-Range Communication:**
  Enables data transmission over long distances without the need for internet, Wi-Fi, or cellular networks.

*  **Integrated GPS Module:**
  Provides accurate location tracking by capturing real-time **latitude and longitude**, especially during emergency situations.

*  **Wearable & Lightweight Design:**
  Designed for comfort and ease of use, making it suitable for long-duration trekking and outdoor activities.

*  **NFC/RFID-Based User Identification:**
  Each watch contains a unique NFC/RFID tag to identify the user within the system.

*  **Checkpoint Interaction:**
  Automatically interacts with pole-based NFC readers to log checkpoint crossings.

*  **SOS Emergency Push Button:**
  Allows the user to instantly send an emergency alert in critical situations.

*  **Real-Time Data Transmission:**
  Sends movement data, SOS alerts, and GPS location information to the system in real time.

*  **Low Power Consumption:**
  Optimized for extended operation using battery power, ensuring long-lasting performance in off-grid environments.

* LoRa Communication:
Enables long-range, low-power wireless communication with the control panel without relying on cellular networks or Wi-Fi.

* Checkpoint-Based Installation:
Installed at regular intervals (approximately 5–10 km) to act as tracking and verification checkpoints along the route.

* Automatic Danger Detection
The AI continuously analyzes movement, location stability, and sensor data. If a person stays at the same place for an abnormal amount of time or shows unusual behavior, the system automatically detects a possible danger situation and triggers an alert.

* Behavior Pattern Analysis
The AI learns normal movement patterns, walking behavior, and route habits of each user to identify deviations that may indicate injury, unconsciousness, or being trapped.

* No-Movement and Stuck Detection
The system uses AI to detect long inactivity, sudden stops, or abnormal motion patterns, even if the user is unable to press the SOS button.

* Smart SOS Validation
The AI filters accidental or false SOS button presses by checking recent activity, motion data, and context before forwarding the alert.

* Context-Aware Decision Making
The AI considers time, location, checkpoint history, and recent sensor activity to decide whether a situation is normal or dangerous.

* Local and On-Device AI Processing
All AI runs on the device or local base station, ensuring fast response, privacy, and zero dependency on internet or cloud.

* Anomaly Detection Engine
The system uses machine learning models to detect abnormal behavior patterns that differ from normal user activity.

* NFC/RFID Reader Integration:
Identifies users by scanning the NFC/RFID tag embedded in the wearable watch when they pass a pole.

* Emergency SOS Push Button:
Allows users to manually trigger an emergency alert at the pole in critical situations.

* ESP32 Microcontroller:
Handles data processing, NFC/RFID scanning, and LoRa data transmission efficiently.

* Outdoor & Mountain-Ready Design:
Designed for reliable operation in harsh outdoor and mountainous environments.


---

##  Working of the System

The Off-Grid Tracker & Emergency Alert System operates through coordinated interaction between the control panel, tracking poles, and smart tracking watches. The system enables continuous monitoring, checkpoint-based tracking, and emergency response without relying on the internet or mobile networks.

---

### **1. Control Panel**


The Control Panel acts as the **central monitoring and decision-making unit** of the system.

**Components:**

* **ESP32:** Main processing and control unit
* **LoRa Module:** Long-range communication with poles and watches
* **OLED Display:** Real-time status and alert visualization

**Functions:**

* Receives data from tracking poles and smart watches
* Displays the **last crossed pole** for each user
* Shows **SOS alerts along with exact GPS coordinates (latitude & longitude)**
* Monitors user movement, progress, and system status in real time

---

### **2. Tracking Poles**

Tracking poles serve as **checkpoint units**, installed at regular intervals (approximately **5–10 km**) along the route.

**Components:**

* **ESP32:** Data processing and control
* **LoRa Module:** Communication with the control panel
* **NFC/RFID Reader:** User identification via watch
* **SOS Push Button:** Manual emergency alert trigger

**Functions:**

* Detect users when they reach a checkpoint using NFC/RFID scanning
* Forward **User ID, Pole ID, and Timestamp** to the control panel
* Allow users to trigger an SOS alert directly from the pole if required

---

### **3. Smart Tracking Watch**

Each user is provided with a smart tracking watch for **personal safety and location tracking**.

**Components:**

* **Arduino Nano:** Processing unit
* **LoRa Module:** Long-range data transmission
* **NFC/RFID Tag:** Unique user identification
* **GPS Module:** Accurate location tracking
* **SOS Push Button:** Emergency alert

**Functions:**

* User taps the watch near a pole to log checkpoint crossing
* Watch transmits **user ID and real-time GPS location** to the nearest pole via LoRa
* The pole forwards this data to the control panel
* In emergencies, pressing the SOS button sends an **instant alert with GPS coordinates**

---

### **4. Real-Time Tracking & Monitoring**

The system continuously updates and displays:

* User location and route progress
* Last crossed checkpoint
* Active SOS alerts with GPS coordinates

This enables quick identification of missing users and ensures that trekkers remain on the correct route.

---

### **5. Emergency Handling**

**SOS Alert Flow:**

1. User presses the SOS button on the watch or at a tracking pole
2. The LoRa module transmits the SOS alert along with GPS location data
3. The control panel receives and displays the alert
4. Rescue teams are notified with the **exact last known location**

### **6. Internet-Independent Operation**

* The entire system operates **without internet, Wi-Fi, or mobile networks**
* **LoRa technology** enables long-range, low-power communication
* Suitable for **remote, mountainous, and disaster-prone environments**

---

##  System Flowchart (Operational Workflow)
<img width="853" height="1280" alt="image" src="https://github.com/user-attachments/assets/baffb48c-6094-4cfd-8dac-2245216b5d9d" />




---

##  Data Flow Diagram (DFD)
<img width="853" height="1280" alt="image" src="https://github.com/user-attachments/assets/16f574b9-6139-4a67-ba87-5b5ccd283302" />


The Data Flow Diagram (DFD) represents how data moves through the Off-Grid Tracker & Emergency Alert System, from the user to the rescue authorities. It highlights the interaction between the wearable watch, tracking poles, communication layer, and control panel in an off-grid environment.



---

###  DFD – Explanation

* **User:**
  The user wears the smart tracking watch and can trigger an SOS alert when needed.

* **Smart Tracking Watch:**
  Collects GPS coordinates, holds the NFC/RFID-based unique ID, and sends user data or SOS alerts using LoRa communication.

* **Pole Checkpoint:**
  Acts as a checkpoint that scans the NFC/RFID tag from the watch and forwards user data along with pole ID and timestamp.

* **LoRa Communication Layer:**
  Enables long-range, low-power, internet-independent data transfer between system components.

* **Control Panel:**
  Receives and analyzes incoming data, displays real-time user status, GPS coordinates, and alerts on the OLED screen.

* **Emergency Decision Module:**
  Validates SOS alerts, identifies the last crossed pole, and prepares actionable information.

* **Rescue Team / Authorities:**
  Receive verified emergency information to initiate fast and accurate rescue operations.

---

##  Challenges


*  **Power Supply in Remote Areas**
  Ensuring uninterrupted power for poles, control panels, and wearable devices is challenging. Solar-powered systems are highly dependent on weather conditions such as limited sunlight, rain, or snow.


*  **Hardware Dependency and Reliability**
  The system relies on multiple hardware components such as ESP32, Arduino Nano, LoRa modules, GPS modules, and NFC readers. Failure of any single component can impact overall system performance.

*  **Device Durability in Extreme Conditions**
  Poles and wearable devices must withstand harsh environmental conditions including rain, snow, dust, extreme temperatures, and physical impact, which increases design and maintenance complexity.


*  **Environmental Interference with LoRa Signals**
  Natural obstacles, atmospheric conditions, and electromagnetic interference may degrade LoRa signal quality, affecting data transmission reliability.

---

