# 📡 ESP8266 WiFi Deauther & Probe Request Attacker

A compact and powerful tool built using an ESP8266 microcontroller to perform **WiFi deauthentication attacks** and **probe request flooding** for penetration testing and educational demonstrations.

---

## 🚀 Features

* 📶 Scan nearby 2.4GHz WiFi networks and clients
* 🛑 Perform Deauthentication (Deauth) Attacks
* 🔍 Send mass Probe Requests to simulate fake clients
* 🧠 Built with Arduino IDE using `.ino` code
* 💡 Simple Web Interface (Optional)
* 🔧 Works on popular ESP8266 boards (e.g. NodeMCU, Wemos D1 Mini)

---

## 🧰 Requirements

* ESP8266 board (NodeMCU, Wemos D1 Mini, etc.)
* Arduino IDE installed
* Required libraries:

  * `ESP8266WiFi.h`
  * `ESP8266WebServer.h`
  * `WiFiClient.h`
  * `DNSServer.h`
* Micro-USB Cable
* (Optional) 3.3V battery for portable operation

---

## 📁 Project Structure

```
esp8266-wifi-deauther/
├── Deauther.ino           # Main Arduino code for WiFi attacks
├── README.md              # Project documentation
└── data/                  # (Optional) Files for web interface
```

---

## 🔧 Installation & Flashing

### Step 1: Install ESP8266 Board Support

* Open **Arduino IDE**

* Go to `File` > `Preferences`

* Add the following URL in **Additional Board Manager URLs**:

  ```
  http://arduino.esp8266.com/stable/package_esp8266com_index.json
  ```

* Then go to `Tools` > `Board` > `Boards Manager`
  Search for **ESP8266** and install it.

### Step 2: Install Required Libraries

Install the following libraries from **Library Manager**:

* `ESP8266WiFi`
* `ESP8266WebServer`
* `DNSServer`

### Step 3: Flash the Code

1. Open `Deauther.ino` in Arduino IDE.
2. Select board: `Tools > Board > NodeMCU 1.0 (ESP-12E Module)`
3. Select COM port: `Tools > Port > [Your COM Port]`
4. Upload the sketch: `Sketch > Upload`

---

## 💥 How It Works

1. **WiFi Scanning**: The ESP8266 scans for nearby WiFi Access Points and connected clients.
2. **Deauth Attack**: Sends forged deauthentication packets to disconnect clients from APs.
3. **Probe Flooding**: Simulates fake devices trying to connect by sending many probe requests with random MAC addresses.

These techniques exploit flaws in the 802.11 WiFi protocol and can be used to demonstrate:

* Network denial-of-service (DoS)
* Rogue access point detection
* WiFi security auditing

---

## 🖥️ Optional Web Interface

This project can be enhanced with a simple web UI for:

* Selecting targets
* Starting/stopping attacks
* Viewing nearby networks

To add a web interface:

* Use `ESP8266WebServer` and host HTML/CSS from SPIFFS or LittleFS
* Upload `data/` folder using Arduino IDE’s **ESP8266 Sketch Data Upload Tool**

---

## ⚠️ Legal Disclaimer

> This tool is for **educational and ethical hacking** purposes only.
> Do **NOT** use this on networks you don’t own or have explicit permission to test.
> The misuse of this software can lead to criminal charges. You are solely responsible for your actions.

---

## 📸 Screenshots

![Screenshot_2023-09-09_133754](https://github.com/user-attachments/assets/28e9ba50-c8f9-44d1-b9e8-3d06ce983a71)

---

## 🧠 Future Improvements

* Add support for ESP32
* Improve attack stability and timing
* Extend web UI for target selection
* Add logging and SSID cloning

---

## 🤝 Acknowledgements

Inspired by:

* [Spacehuhn's WiFi Deauther](https://github.com/SpacehuhnTech/esp8266_deauther)
* ESP8266 Community Libraries

---

## 📜 License

This project is licensed under the MIT License. See `LICENSE` file for more info.
