# LED Badge Firmware

Offizielle Firmware für das LED Badge. Die Firmware-Dateien gibt es unter [Releases](https://github.com/markdaswolf/led-badge-firmware/releases).

Jedes Release enthält:

| Datei | Wofür |
| --- | --- |
| `firmware.bin` | Update über die App |
| `LED-Badge-vX.Y.Z-full.bin` | Manuelles Flashen per USB |
| `LED-Badge-vX.Y.Z-source.zip` | Quellcode, siehe [Lizenz](#lizenz) |
| `SHA256SUMS.txt` | Prüfsummen der Dateien |

## Update über die App

1. Am Badge die Boot-Taste 3 Sekunden halten, bis die Status-LED cyan atmet.
2. In der App mit dem Badge verbinden.
3. Das Badge muss mit einem WLAN mit Internetzugang verbunden sein (App → Netzwerk → WLAN-Client).
4. App → System → **Nach Updates suchen**, dann **Version … installieren**.

Das Badge lädt die Firmware, startet neu und ist danach wieder per Bluetooth erreichbar. Mit „Automatische Updates“ im Netzwerk-Tab prüft das Badge selbst beim Start und alle 6 Stunden.

## Manuelles Update per USB

1. `LED-Badge-vX.Y.Z-full.bin` aus dem gewünschten Release herunterladen.
2. Badge per USB-C mit dem Computer verbinden.
3. Flashen, entweder im Browser oder mit esptool:
   - **Browser (Chrome oder Edge):** [ESP Tool](https://espressif.github.io/esptool-js/) öffnen, auf *Connect* klicken und das Badge wählen. Als Flash Address `0x0` eintragen, die Datei auswählen und *Program* klicken.
   - **esptool:**
     ```
     esptool.py --chip esp32s3 write_flash 0x0 LED-Badge-vX.Y.Z-full.bin
     ```
4. Nach dem Flashen kennt das Badge gekoppelte iPhones nicht mehr. Am iPhone unter *Einstellungen → Bluetooth* das Badge ignorieren und in der App neu koppeln. Display-Inhalte und Einstellungen bleiben erhalten.

## Eigene Update-Quelle

Unter App → System → **Update-Quelle** lässt sich statt dieses Repositorys ein eigener Link setzen, zum Beispiel ein anderes GitHub-Repository (`https://github.com/name/repo`), dessen Releases eine `firmware.bin` enthalten. Ein leerer Link stellt die Standard-Quelle wieder her.

## Lizenz

Die Firmware ist proprietär und nur für die private, nicht kommerzielle Nutzung auf freigegebener LED-Badge-Hardware lizenziert, siehe [LICENSE](LICENSE). Der Quellcode liegt jedem Release bei, damit die enthaltenen LGPL-Komponenten ausgetauscht werden können. Das macht die Firmware nicht zu Open Source.

Enthaltene Komponenten von Drittanbietern und ihre Lizenzen stehen in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
