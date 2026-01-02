| BluScreen Control Hub |

BluScreen Control Hub is a web-based control panel used to connect to and control the BluScreen Smart Display via Bluetooth Low Energy (BLE).
It allows you to send commands to the BluScreen ESP32 device using voice input or typed text, which are then displayed or processed by the BluScreen system.

Setup Features:
1. 🔌 Wireless BLE connection to BluScreen (ESP32)
2. 🎙 Voice-to-text control using browser speech recognition
3. ⌨ Manual text input for precise commands
4. 📡 Real-time command transmission to BluScreen
5. 💻 Fully browser-based (no app installation)
6. WiFi/ Router required

BluScreen Features:
1. 🕒 Real-Time Clock – Displays current time in 12-hour or 24-hour format
2. 📅 Date Display – Shows current date with day, month, and year
3. 🌦 Weather Information – Displays live weather conditions
4. 🌡 Temperature Display – Shows ambient or fetched temperature data
5. ⏱ Timers – Start, stop, and reset countdown timers
6. 🔔 Task Reminders – Set reminders to notify or display messages at specific times
7. 📝 Custom Text Display – Show user-entered messages on the LED matrix
8. 💡 Brightness control- Control the light intensity of the display using the brightness slider
   
Requirements:
- Hardware
BluScreen device powered by an ESP32. ESP32 advertising with Bluetooth name starting with BluScreen
- Software
A Chromium-based browser (Google Chrome / Edge / Brave recommended). Bluetooth enabled on the device. HTTPS or localhost (required for Web Bluetooth & Speech API)

⚠ You must connect your BluScreen to the internet/ router before sending any commands (time, date, weather, temperature). Add your router details in the ESP32 code before uploading the code into the ESP32. 

How to Use:
1. Open the Webpage
Open the BluScreen Control Hub webpage in a supported browser.

2. Connect to BluScreen
Click 🔌 Connect ESP32
Select the BluScreen device from the Bluetooth popup
Wait for the confirmation alert (✅ Connected to ESP32!)
⚠ You must connect before sending any commands.

3. Send Commands
   
🎙 Voice Mode
- Click Record
- Speak your command clearly
- The recognized text will appear on screen
- Click Send to ESP32 to transmit it
- Example voice command: "Show temperature"

⌨ Type Mode
- Click Type
- Enter your command in the text box
- Click Send to ESP32
- Example typed command: "Start timer 10 minutes"

Supported Browsers Browser	BLE	Voice
- Chrome	✅
- Edge	✅	
- Brave  ✅
- Firefox	❌	
- Safari	❌	⚠ Limited

Brightness Control:

BluScreen includes a brightness slider that allows the user to control the LED display intensity in real time. Using this slider, the brightness of the display can be smoothly adjusted across safe levels supported by the hardware, making the screen comfortable to view in different lighting conditions such as daylight or dark rooms. The brightness command is sent instantly to the ESP32, which updates the display intensity without interrupting any ongoing features like time, reminders, or messages. This helps reduce eye strain, saves power, and gives the user better control over the overall viewing experience.

Quick Action Buttons

BluScreen also provides four quick action buttons for commonly used display commands: Time, Date, Weather, and Temperature. These buttons eliminate the need to manually type commands, making the interface faster and more user‑friendly. With a single click, the selected information is immediately shown on the display via BLE communication. This feature is especially useful for quick access and demonstrates seamless integration between the web interface and the ESP32 device.

Bluetooth Details (For Developers):

* Service UUID: 12345678-1234-5678-1234-56789abcdef0
* Characteristic UUID: abcdef01-1234-5678-1234-56789abcdef0

Data is sent as UTF-8 encoded text

Notes & Limitations:

Voice recognition depends on browser support.
Internet is required for speech recognition.
Commands are sent as plain text. Parsing happens on the ESP32. Page must remain open while connected

Project Context:

BluScreen Control Hub is part of the BluScreen Smart Display System, an IoT-based LED matrix display capable of showing time, date, weather, reminders, timers, and custom text using Wi-Fi and BLE connectivity.
