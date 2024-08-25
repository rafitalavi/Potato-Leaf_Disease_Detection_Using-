Industrial Protection System with SMS Notification Using GSM Module

This project aims to build a smart industrial protection system that monitors temperature, humidity, and gas leakage. The system uses a DHT22 sensor for temperature and humidity readings, a gas sensor to detect gas leakage, and a GSM module (SIM900A) to send SMS alerts when certain conditions are met. It also controls relays to shut down machinery or trigger alarms in case of an emergency.
Features

    Temperature and Humidity Monitoring: Uses a DHT22 sensor to measure the ambient temperature and humidity levels.
    Gas Leakage Detection: Monitors gas levels using a gas sensor and detects any leakage or unsafe conditions.
    SMS Alerts: Sends SMS alerts to a predefined mobile number using a GSM module (SIM900A) when overheating or gas leakage is detected.
    Relay Control: Controls relays to activate/deactivate machinery or alarms based on sensor data to prevent accidents.
    LCD Display: Displays real-time data and alerts on a 16x2 LCD screen for on-site monitoring.

Components Used

    Arduino: The microcontroller platform used to run the code and control sensors and relays.
    SIM900A GSM Module: Used to send SMS alerts when critical conditions are detected.
    DHT22 Sensor: Measures temperature and humidity.
    Gas Sensor (MQ series): Detects gas leakage.
    Relay Modules: Used to control external devices or machinery.
    16x2 LCD Display: Provides a visual display of temperature, humidity, gas levels, and alert messages.

How It Works

    Initialization: The system initializes the sensors, GSM module, and LCD display upon startup.
    Data Reading: Continuously reads temperature, humidity, and gas levels.
    Condition Check: Checks if the temperature exceeds a threshold (e.g., 36°C) or if gas levels exceed a safe limit (e.g., a sensor reading above 450).
    Alerts and Actions:
        If overheating or gas leakage is detected, the system sends an SMS alert and activates the corresponding relays to shut down machinery or trigger alarms.
        Displays alerts on the LCD screen for local monitoring.
    Status Updates: Periodically sends status updates via SMS, indicating that the system is functioning normally.

How to Use

    Hardware Setup:
        Connect the DHT22 sensor to the Arduino's digital pin 2.
        Connect the gas sensor to the Arduino's analog pin A0.
        Connect the relays to digital pins 9 and 7.
        Connect the SIM900A GSM module to digital pins 10 and 11 (SoftwareSerial).
        Connect the 16x2 LCD display using I2C protocol (address 0x27).

    Software Setup:
        Install the necessary Arduino libraries: DHT, SoftwareSerial, and LiquidCrystal_I2C.
        Upload the provided Arduino sketch to your Arduino board.

    Run the System:
        Power up your Arduino and connected components.
        Monitor the LCD for real-time temperature, humidity, and gas level readings.
        Receive SMS alerts on your mobile phone in case of any emergency.

Dependencies

    Arduino IDE
    Adafruit Unified Sensor Library
    DHT Sensor Library
    SoftwareSerial Library
    LiquidCrystal_I2C Library
