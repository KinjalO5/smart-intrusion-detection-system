#  Smart Intrusion Detection System (IoT Project)

This IoT project uses a **PIR sensor** to detect human motion and trigger a **real-time alert** using the **Blynk cloud platform**. The system also provides a **local visual alert** using an LED. It is fully simulated using **Wokwi** with an **ESP32** microcontroller.

---

##  Project Objective

> To develop a Smart Intrusion Detection System using NodeMCU (ESP32), PIR sensor, and LED, with cloud-based alerts via Blynk.

---

## 🔧 Features

-  Motion detection using PIR sensor
-  LED turns ON when motion is detected
-  Sends real-time alert to Blynk Cloud (simulated)
-  Fully simulated in Wokwi for testing

---

##  Hardware Components

| Component     | Description                     |
|--------------|---------------------------------|
| ESP32         | Microcontroller (used instead of NodeMCU) |
| PIR Sensor    | For human motion detection      |
| LED           | For visual alert                |
| Internet      | Required for real Blynk alerts  |

>  **Note**: ESP8266 NodeMCU is not available in Wokwi, so **ESP32** is used — which is compatible and performs the same function.

---

##  Working Principle

1. System initializes and connects to WiFi via Blynk.
2. PIR sensor continuously checks for motion.
3. If motion is detected:
   - LED turns ON
   - Serial Monitor prints “Motion Detected!”
   - Blynk event is triggered (`intrusion`)
4. If no motion is detected:
   - LED turns OFF

---

##  Simulation Link

🔗 **[Click here to run the simulation on Wokwi](https://wokwi.com/projects/399594436845783041)**

---

##  Flowchart (Code Logic)

```mermaid
graph TD
A[Start] --> B[Initialize Blynk & Components]
B --> C[Read PIR Sensor Input]
C --> D{Motion Detected?}
D -- Yes --> E[Turn ON LED]
E --> F[Send Alert via Blynk]
F --> C
D -- No --> G[Turn OFF LED]
G --> C


  
