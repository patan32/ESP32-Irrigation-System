I am using Open-Meteo for weather. Entity is "weather.home". Make sure in states you have entity called: "home_rain_forecast_0d" or else it won't work. I had to use Meteorologisk institutt (Met.no) for humdity reading since Open-Meteo doesn't provide that entity. 

Change your weather entity name from HA for weather to work properly. Look for weather.forecast_home entity and change it to what you have in HA for weather. 
automation.yaml - updates the NZ holiday days. 
sensors.yaml - All sensors are defined and needs the entity changed to match yours in HA. 

🌱 ESPHome Smart Irrigation Controller

Fully local, highly reliable, feature-rich smart irrigation controller built using ESPHome + Home Assistant.
---------------------------------------
✨ Key Features
---------------------------------------

---------------------------------------
🚿 Irrigation Control
---------------------------------------

Multi-zone irrigation management

Independent scheduling per zone

Manual start / stop for each zone

Master valve support

Adjustable watering duration per zone

Zone sequencing with configurable delays

Auto zone switching

Pause / resume irrigation cycles

Global irrigation enable / disable

---------------------------------------
💧 Flow Monitoring & Protection
---------------------------------------

Real-time water flow monitoring

Automatic flow calibration (pulse-per-litre)

Per-zone water usage tracking

Total water consumption tracking

Leak detection with automatic shutoff

Low-flow detection (blocked pipe / faulty valve)

High-flow detection (burst pipe / stuck valve)

Runtime-based flow verification

Flow alarms & notifications

🌦 Smart Weather Logic

Rain probability integration

Rain skip / rain delay logic

Temperature-based watering lockout

Seasonal watering adjustment

Smart irrigation scaling

---------------------------------------
📊 Sensors & Monitoring
---------------------------------------
Temperature monitoring

Humidity monitoring

Water flow monitoring

Daily / weekly / monthly water usage stats

System uptime monitoring

WiFi signal monitoring

---------------------------------------
🧠 Automation & Logic
---------------------------------------
Advanced Home Assistant automation support

Smart scheduling logic

Conditional watering rules

Runtime verification

Automatic fault recovery

Scheduled alarm reset

---------------------------------------
🌐 Web Interface & UI
---------------------------------------
Built-in ESPHome web server

Mobile-friendly UI

Real-time valve status

Live flow monitoring

Countdown timers

Error & fault indicators

---------------------------------------
📱 Home Assistant Integration
---------------------------------------
Native ESPHome API

Full entity exposure

OTA updates via Home Assistant

100% local operation

Lovelace dashboard ready

---------------------------------------
🔐 Reliability & Safety
---------------------------------------
Fail-safe valve shutdown

Watchdog protection

Brownout detection

Safe boot mode

Power-loss recovery

---------------------------------------
🧰 Hardware Requirements
Required
---------------------------------------
ESP32 Development Board

Relay board / MOSFET valve drivers

Water Flow Sensor

Hall-effect water flow sensor: YF-B5

The YF-B5 sensor is used for real-time flow measurement, water usage tracking, leak detection, and flow safety automation.
