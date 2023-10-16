# Tag Connect KiCad Symbols and Footprints
Easy to use schematic symbols and PCB footprints for Tag Connect programming headers.

# Why Tag Connect?
See [this post](https://nawo.tech/the-standard-esp32-header) for background/ info.

# Symbols
| Symbol Name       | For Micro(s)
| ------------- |-------------|
| TC2030-IDC    | Any |
| TC2030-IDC_ESP    | ESP32 |
| TC2030-IDC_Cortex-M    | ARM Core, SWD |
| TC2050-IDC_Cortex-M    | ARM Core, Full JTAG |

# How to use
1. Clone this repo to your computer
2. Open Symbol Editor from KiCad home screen, File -> Add Library -> Select `Tag-Connect.lib`
3. Open footprint Editor from KiCad home screen, File -> Add Library -> Select `Tag-Connect.pretty` folder
4. Use the desired symbol in your next schematic
5. Click the symbol -> edit -> choose footprint -> search "TC2030" or "TC2050" and select the footpint mathcing your cable
