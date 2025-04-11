# Smart Solar Heater Controller with Relays

## Project Overview
This project is a smart solar-powered heating system that dynamically diverts excess solar energy into a 6kW heating element. It uses an ESP32-WROOM-32D microcontroller, a DS18B20 temperature sensor, and a XTR115 current transmitter to control the heating element based on surplus energy and temperature. The system also allows for controlling up to 3 additional devices using relays, all managed through Home Assistant for remote control and monitoring.

---

## Features

- **Dynamic Heating Control**: Diverts excess energy into the heating element, proportional to available solar power.
- **Temperature-based Control**: The heater operates only when the temperature is below 50°C and shuts off above 50°C.
- **Relay Control**: Includes 3 relays to control external devices (e.g., fan, pump).
- **Adjustable DAC Range**: Configurable voltage range for controlling the heater (e.g., 0V–3.3V = 4–20mA).
- **Home Assistant Integration**: Remote control and monitoring of the system via Home Assistant.
  
---

## Components Used

- **ESP32-WROOM-32D**: Main microcontroller for control and communication.
- **XTR115**: Voltage-to-current transmitter, generating the 4–20mA signal to control the heating element.
- **DS18B20**: Temperature sensor for temperature monitoring of the heating system.
- **3x Relays**: Used for controlling external devices.
- **Huawei EMMA**: Energy monitor to track the excess solar power per phase.

---

## Folder Structure

```plaintext
Smart-Solar-Heater-Controller/
│
├── hardware/
│   ├── schematic/               # Schematic diagrams for the device
│   ├── layout/                  # PCB layout (Gerber files, etc.)
│   ├── datasheets/              # Datasheets for components used
│   ├── additional_components/   # Documentation for any extra components
│   └── fabrication_data/        # Fabrication and assembly instructions
│
├── software/
│   ├── esphome/                 # ESPHome YAML configuration files
│   │   └── heater_controller.yaml  # Main ESPHome configuration for the device
│   ├── homeassistant/           # Home Assistant templates and automation scripts
│   │   └── automation.yaml     # Home Assistant automations for controlling the heater
│   └── README.md               # Software-specific README with setup instructions
│
├── documentation/
│   ├── README.md               # Overall project documentation
│   └── wiring_diagrams/        # Wiring diagram image files
│
└── LICENSE                     # License for the project (e.g., MIT)
