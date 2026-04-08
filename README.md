# Cybersecurity : CSN150
Project: ESP32 Camserver

## Purpose
Set up ESP32 and Arduino enviornment. Execute sketch " Wifiscanner". 

## Equipment
* [ESP32Cam](https://www.amazon.com/Aideepen-ESP32-CAM-Bluetooth-ESP32-CAM-MB-Arduino/dp/B08P2578LV/ref=sr_1_3?crid=4FY0ECFW0ZX7&keywords=ESP32+Cam&qid=1678902050&sprefix=esp32+cam%2Caps%2C240&sr=8-3)

* [USB Micro Data Cable](https://www.amazon.com/AmazonBasics-Male-Micro-Cable-Black/dp/B0711PVX6Z/ref=sr_1_1_sspa?keywords=micro+usb+data+cable&qid=1678902214&sprefix=Micro+USB+data+%2Caps%2C89&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUFaU0NaUVZHU1RFUlAmZW5jcnlwdGVkSWQ9QTA3NTA4MDVFVERCS01HVlgxM1YmZW5jcnlwdGVkQWRJZD1BMDE4NTE1NTIwWUdONkdWSzU1M1Amd2lkZ2V0TmFtZT1zcF9hdGYmYWN0aW9uPWNsaWNrUmVkaXJlY3QmZG9Ob3RMb2dDbGljaz10cnVl)
* A computer with Arduino IDE installed
* A WI-FI Connection: (You have to know the SSID and password)

## Links to documentation and tools

https://lastminuteengineers.com/getting-started-with-esp32-cam/ 

##### Video 1: 
https://www.youtube.com/watch?v=RCtVxZnjPmY

##### AI GPTs used
CHATGPT:
GOOGLE AI: 
## Steps I followed
1. First Step should be making sure Arduino IDE is properly configured
2. In order to view ESP32 boards you have to go to File > Preferences and add "https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json" url to "Additional Boards Manager URLs:
3. You can now install the ESP32 packages: You go to Tools > Board > Boards Manager and search for "ESP32" and install the package by Espressif systems.
4. Now you can select your board make sure your ESP32-Cam is plugged into your computer and then go to Tools > Board > ESP32 Arduino and select AI Thinker ESP32-CAM and Select the proper port
5. Now you can start the project
6. You have to open the proper example project for CameraWebServer: To open the example go to File > Examples > ESP32 > Camera > CameraWebServer
7. You are going to have to select the camera model in the example code: You will see multiple tabs you want to look at the tab board_config.h
8. You have to uncommet "CAMERA_MODEL_AI_THINKER" (uncommet is deleting the "//" next to line where #define CAMERA_MODEL_AI_THINKER) and comment every other model
9. After thats done go to the CameraWebServer.ino tab in the example code, you have to input your SSID and PASSWORD of your WIFI credentials in the " "
10. You would fill your SSID and PASSWORD in the Black spaces. <img width="394" height="60" alt="image" src="https://github.com/user-attachments/assets/45f15b32-34bc-4fcf-b0f8-7af20b593615" />


## Problems and Solutions
Note your problems or errors here.  Google any error you may come across, and not what you tried (even if it does not work), and what was the final answer. Document your errors and solutions that worked for you.  

**Problem:** E (485) camera: Camera probe failed with error 0x105(ESP_ERR_NOT_FOUND)
Camera init failed with error 0x105
**Solution:**

### Example Problem
**Problem:** Arduino code will not load on ESP32 Cam.
**Solution:** Camera drivers were incorrect I needed to install the driver: [https://www.wch-ic.com/downloads/CH341SER_ZIP.html](https://github.com/martin-ger/esp32_nat_router).  I used file, "CH341SER.ZIP" and it worked.

## Final Report
