# Cybersecurity : CSN150
Project: ESP32 Camserver

## Purpose
Set up ESP32 and Arduino enviornment. Execute sketch " CAMSERVER". 

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
10. You would fill your SSID and PASSWORD in the Black spaces.
11. <img width="394" height="60" alt="image" src="https://github.com/user-attachments/assets/45f15b32-34bc-4fcf-b0f8-7af20b593615" />
12. Now you should be able to upload and run the code, double checking your ESP32-CAM is plugged in using either a Micro-usb or USB-C cable to your computer 
13. Hit upload -> The arrow icon is the upload button <img width="37" height="32" alt="image" src="https://github.com/user-attachments/assets/7e90f0c6-f687-4228-8a7f-869fd08fe22e" />
14. Now if you don't get any errors in compling you can click on serial monitor button which looks like > <img width="46" height="46" alt="image" src="https://github.com/user-attachments/assets/e8b2e757-e2a3-431a-8b4a-68f670555c41" />
15. When you open Serial Monitor you can set bauds make sure you set it 115200 which is the number dictated in teh example
16. If you don't see an output don't be alarmed on the ESP32-CAM board you should be able to see a reset button, after you press it and wait a bit you should be able to see an output which gives you an ipaddress
17. Entering the IPADDRESS in the search bar of any browser pulls up a GUI of streaming software, to make sure the code is working properly hit start streaming and you should see the display pop up with live feed


## Problems and Solutions
Note your problems or errors here.  Google any error you may come across, and not what you tried (even if it does not work), and what was the final answer. Document your errors and solutions that worked for you.  

## Issue 1: Camera model not selected
Error:
#error "Camera model not selected"

Fix:
Defined camera model:
#define CAMERA_MODEL_AI_THINKER

## Issue 2: No Camera Output
Cause: Wrong board selected
Fix: Selected "AI Thinker ESP32-CAM" in Arduino IDE

## Final Report
In this project, I built a simple webcam that can be streamed online using the ESP32-CAM and the Arduino IDE. I had to make sure set up was done correctly if not all is fornaught. I initially encountered an error indicating that the camera model was not selected, which I fixed by properly defining it in the proper section. I used a YouTube video and some written tutorials to guide me through the setup and used gpt to troubleshoot problems. One challenge that took me a while to figure out was writing the SSID and password without proper capitalization which resulted on it not functioning properly. Another was ensuring the correct board was selected. This project helped me understand the amount of work that it actually takes to properly connect hardware and software to work together over wifi. In the future, I could improve this project by adding features such as facial recongition like in my others professor class using teachablemachine. 




















