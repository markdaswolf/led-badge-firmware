# Third-Party Notices

The LED Badge firmware contains the following third-party components. They remain under their own licenses; the [LED Badge Firmware License](LICENSE) does not restrict the rights those licenses grant. The full license texts are in [third-party-licenses](third-party-licenses).

| Component | License | License text |
| --- | --- | --- |
| [Arduino core for ESP32](https://github.com/espressif/arduino-esp32) | LGPL-2.1 | [LGPL-2.1.txt](third-party-licenses/LGPL-2.1.txt) |
| [ESP-IDF](https://github.com/espressif/esp-idf) (prebuilt in the Arduino core, incl. mbedTLS) | Apache-2.0 and others, see the ESP-IDF repository | [Apache-2.0.txt](third-party-licenses/Apache-2.0.txt) |
| [ESPAsyncWebServer](https://github.com/me-no-dev/ESPAsyncWebServer) | LGPL-3.0 | [ESPAsyncWebServer-LGPL-3.0.txt](third-party-licenses/ESPAsyncWebServer-LGPL-3.0.txt), [GPL-3.0.txt](third-party-licenses/GPL-3.0.txt) |
| [AsyncTCP](https://github.com/me-no-dev/AsyncTCP) | LGPL-3.0 | [AsyncTCP-LGPL-3.0.txt](third-party-licenses/AsyncTCP-LGPL-3.0.txt), [GPL-3.0.txt](third-party-licenses/GPL-3.0.txt) |
| [NimBLE-Arduino](https://github.com/h2zero/NimBLE-Arduino) | Apache-2.0 | [NimBLE-Arduino.txt](third-party-licenses/NimBLE-Arduino.txt), [NOTICE](third-party-licenses/NimBLE-Arduino-NOTICE.txt) |
| [FastLED](https://github.com/FastLED/FastLED) | MIT | [FastLED.txt](third-party-licenses/FastLED.txt) |
| [ArduinoJson](https://github.com/bblanchon/ArduinoJson) | MIT | [ArduinoJson.txt](third-party-licenses/ArduinoJson.txt) |
| [Adafruit EPD](https://github.com/adafruit/Adafruit_EPD) | MIT | [Adafruit-EPD.txt](third-party-licenses/Adafruit-EPD.txt) |
| [Adafruit GFX Library](https://github.com/adafruit/Adafruit-GFX-Library) | BSD | [Adafruit-GFX.txt](third-party-licenses/Adafruit-GFX.txt) |
| [Adafruit BusIO](https://github.com/adafruit/Adafruit_BusIO) | MIT | [Adafruit-BusIO.txt](third-party-licenses/Adafruit-BusIO.txt) |
| [U8g2 for Adafruit GFX](https://github.com/olikraus/U8g2_for_Adafruit_GFX) (incl. U8g2 fonts) | BSD-2-Clause, fonts under their individual licenses | [U8g2_for_Adafruit_GFX.txt](third-party-licenses/U8g2_for_Adafruit_GFX.txt) |

## Components under the LGPL

The Arduino core for ESP32, ESPAsyncWebServer and AsyncTCP are licensed under the GNU Lesser General Public License. To meet its requirements:

- Every release contains the complete source code of the firmware (`LED-Badge-vX.Y.Z-source.zip`), so these components can be replaced with modified versions and the firmware rebuilt with [PlatformIO](https://platformio.org) (`pio run`).
- The modified firmware can be installed over USB as described in the [README](README.md).
- Section 5 of the LED Badge Firmware License grants the rights the LGPL requires for this purpose.

The source code of the LGPL components themselves is available at the linked repositories.
