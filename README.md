# 🔌 ESP8266 Web Wake-on-LAN + LCD Weather Display

This project turns your **ESP8266** board into a smart device that:

- 🌐 Hosts a local web server to send **Wake-on-LAN** packets
- 📺 Displays system/network info and **weather data** on a 20x4 I2C LCD
- ⏰ Syncs time using **NTP**
- ☁️ Fetches weather updates via **OpenWeatherMap API**

Inspired by **[Tiratex/WakeOnLan](https://github.com/Tirarex/EspWOL)** and enhanced with real-time weather and system stats!

---

## 🔧 Features

- Send **WOL packets** to wake PCs/devices from the web interface
- Display IP, time, date, free memory on the top half of a 20x4 LCD
- Show weather data (temperature, description) from OpenWeatherMap on the bottom half
- Auto Wi-Fi setup via **WiFiManager**
- Uses **LittleFS** for storing HTML and config

---

## 🧰 Libraries Used

Ensure the following libraries are installed in your Arduino IDE or PlatformIO environment:

```cpp
#include <ESP8266WiFi.h>
#include <ESP8266WebServer.h>
#include <LittleFS.h>
#include <WiFiUdp.h>
#include <WakeOnLan.h>
#include <ArduinoJson.h>
#include <WiFiManager.h>
#include <ESP8266HTTPClient.h>
#include <NTPClient.h>
#include <LiquidCrystal_I2C.h>
