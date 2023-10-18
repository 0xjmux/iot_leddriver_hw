## Important Design Information
* All information about the board needed for development can be found in the [latest release](https://github.com/0xjmux/iot_leddriver_hw/releases/latest)
* Current microcontroller is ESP32-S2-SOLO ([datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-s2-solo-2_esp32-s2-solo-2u_datasheet_en.pdf))
    * We're also attempting to use the [ESP32-S3-WROOM-2](https://www.espressif.com/sites/default/files/documentation/esp32-s3-wroom-2_datasheet_en.pdf) microcontroller during development, because of its dual-core capability. 
*  A MEMS Microphone, the `SPH0641LU4H-1`, can be optionally installed in case we later want to add live sound reactivity capability ([datasheet](https://www.knowles.com/docs/default-source/default-document-library/sph0641lm4h-1-datasheet-rev-f.pdf?Status=Master&sfvrsn=217e70b1_0) ).

#### Pinout

| GPIO PIN | Connected to   |
|----------|----------------|
| `GPIO21` | LED Strip D_in |
| `GPIO2`  | Status LED     |
| `GPIO33` | I2C SDA        |
| `GPIO35` | I2C SCL        |
| `GPIO5`  | MEMS Mic Clock |
| `GPIO6`  | MEMS Mic Data  |

#### Hardware Limitations
* Trace width and vias for power delivery from DC jack to LED Strip Power lines calculated to handle <=15A with ΔT rise of <10°C. 
* Maximum draw of a 5M 60 LED/m WS2812B strip (all white at maximum brightness) is 12A @ 5V. Anything longer than that and you start seeing the brightness drop due to the resistance of the traecs inside the strip, so it is unlikely this design limit will be exceeded. 


#### ESP32-S2-SOLO Information
* [ESP32-S2-SOLO-2 Datasheet pdf](https://www.espressif.com/sites/default/files/documentation/esp32-s2-solo-2_esp32-s2-solo-2u_datasheet_en.pdf)
* [ESP32-S3-WROOM-2 Datasheet pdf](https://www.espressif.com/sites/default/files/documentation/esp32-s3-wroom-2_datasheet_en.pdf), because of its dual-core capability. 
* [esp32-s2_hardware_design_guidelines_en.pdf](https://www.espressif.com/sites/default/files/documentation/esp32-s2_hardware_design_guidelines_en.pdf)
* [esp32-s2_technical_reference_manual_en.pdf](https://www.espressif.com/sites/default/files/documentation/esp32-s2_technical_reference_manual_en.pdf)

#### ESP32-S2-Mini-2 (OLD CHIP) Information
* [esp32-s2-mini-2\_esp32-s2-mini-2u\_datasheet\_en.pdf](https://www.espressif.com/sites/default/files/documentation/esp32-s2-mini-2_esp32-s2-mini-2u_datasheet_en.pdf)

##### ESP32 pin information
* [ESP32 Pinout Reference: Which GPIO pins should you use? | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-pinout-reference-gpios/)

