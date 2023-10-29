# Spotify Neopixel Visualizer Hardware
ESP32-based WS2812B LED Strip Driver, with plans to use the Spotify API to sync and pulse to music. 

![LED Ring Gif](./files/iot_leddriver_v2.1_ledring_stable.gif)

* Board firmware (in progress) can be found [in iot_leddriver_sw](https://github.com/0xjmux/iot_leddriver_sw).
* Optionally, compatible with the popular [WLED](https://github.com/Aircoookie/WLED) firmware: just change the LED data pin to `GPIO21`. 
* (See [DEVELOPMENT-NOTES.md](DEVELOPMENT-NOTES.md) for additional pinout and other information).
 
### Features
* ESP32 based for low-cost IoT Capability, using ESP32-S2-SOLO. 
* Programmable over USB C
* Includes Tag-Connect JTAG header for full JTAG debug capability. 
* Two ways to attach LED strip, including strain relief for wires connecting to the LED Strip. 
* M2 mounting holes, various test pads, and an emergency UART header on the bottom. 
* Includes I2C breakout for optional addition of SSD1306 OLED.
* MEMS Microphone can optionally be added for live sound reactivity. 
* Entirely LCSC BOM, designed for both hand and machine assembly. Able to be assembled by JLCPCB with low-cost components.

## Notes and Usage
* Schematic, BOM, Gerbers, and all other files needed for development or production can be found attached to the latest [release!](https://github.com/0xjmux/iot_leddriver_hw/releases/latest)
* This includes an interactive HTML BOM, which makes hand assembly much easier. 
* See [DEVELOPMENT-NOTES.md](DEVELOPMENT-NOTES.md)

## Versions

### V2.1 - Board updates
* Original ESP32-S2-MINI wasn't hand assembleable, so it's been replaced with an ESP32-S2-SOLO. 
* Various small upgrades, including removal of non-necessary RC components, a mini UART header, and additional 5V power lines right next to the 2.1mm jack for strips with additional power wires. 
* The footprint and supporting components for a MEMS Microphone (SPH0641LM4H-1) added in case live sound reactivity is desired later on. 
![v2.1 PCB Render Front](files/PCB_v2.1_render_F_RayT.png)
![v2 PCB Render Back](files/PCB_v2.1_render_B_RayT.png)
![v2 PCB Layout](files/PCB_v2.1_layout.png)


### V2.0 - Complete redesign, now ESP32 Based
* Board upgraded to the `ESP32-S2-MINI-2-N4` for better compute capability, completely redesigned solely around the WS2812B.
* Most of the features listed above were introduced in this version.
![v2 PCB Render Front](files/PCB_v2.0_render_F.png)
![v2 PCB Render Back](files/PCB_v2.0_render_B.png)
![v2 PCB Layout](files/PCB_v2.0_layout.png)

---
### V1.0 Prototype
* [Link to v1.0 branch](https://github.com/0xjmux/iot_leddriver_hw/tree/v1.0)
* V1 was never fully tested; right as the first version of the hardware was ready the direction of the project shifted, and it wasn't going to have enough compute for use of the spotify API. 
* V1.0 was an IoT enabled LED strip driver using ESP8266 capable of using both WS2812B (Neopixel) and standard 5050 12V LED strips. Goal is to integrate with the spotify API to allow color changes in reaction to music. 
* If board will only be used in 5V (neopixel) mode, then the 3 `UMW30N06` Mosfets and 2 of the `MCP1416` mosfet drivers are not needed. Additionally, if the board will only be run in one mode then the unused 2.1mm jack does not need to be installed. 
![v1 PCB Render Front](files/PCB_v1.0_render_F.png)
![v1 PCB Render Back](files/PCB_v1.0_render_B.png)
![v1 PCB Layout](files/PCB_v1.0_layout.png)
