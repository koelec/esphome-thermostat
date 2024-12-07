# esphome-thermostat
ESPHome yaml config for defining a thermostat to control the GREE versati heat pump by modbus.

This repo is an extension to [ESPHome gree modbus interface](https://github.com/koelec/EspHome-Gree?tab=readme-ov-file).

It contains additional esphome yaml configuration to define a generic thermostat, which can be controlled from the Home Assitant Dashboard or work standalone when deployed on the same ESP32 device as the GREE modbus interface.

Read about Home Assistant's generic thermostat [](https://www.home-assistant.io/integrations/generic_thermostat/) 

The Thermostat needs a room temperature sensor as input and will turn on/off the heat pump by sending commands on the heat pump's modbus interface.

When turning on the heat pump, the code also changes some settings of the HP to be able to run the heat pump without internal thermostat and with 'control state' set to 'water out' mode. 

Next this it will turn on 'silent mode' when outdoor temparature is above 2 degrees and set the WOT-heat temperatuur depending on the outside temperature according to some simple logic.

You can change the logic for both turning on the 'silent mode' and setting the WOT-heat setting by changing the values in the yaml file to suit your own situation.

![image](https://github.com/user-attachments/assets/6d9f2274-8253-4988-8f19-23ad1c8f8e5c)

