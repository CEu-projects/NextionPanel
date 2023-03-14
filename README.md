# NextionPanel

Lightwight UI for NSPanel or other Nextion-Panels connected on an ESP32 with Tasmota firmware.
Inspiration for this project was https://github.com/joBr99/nspanel-lovelace-ui.

Anleitung zur Einrichtung
* einen lokalen Webserver bereitstellen und die Datei NSPanel.tft (siehe HMI/NSPanel.tft) ablegen (z.B. unter http://openhab:9090/NSPanel.tft); dafür nicht den Openhab-internen Webserver nutzen, da dieser hierfür nicht korrekt funktioniert (keine content lenght wird herausgegeben)
* Tasmota NSPanel-Version flashen: http://ota.tasmota.com/tasmota32/release-12.2.0/
* die unter Tasmota/autoexec.be im Tasmota-Filesystem ablegen / austauschen - dabei eventuell die Adresse der NSPanel.tft anpassen
* Neustart und in der Console <b>InstallNSPanel</b> aufrufen

Befehle (können auch gut über http://mqtt-explorer.com/ getestet werden):

Seite anzeigen mit definiertem Namen
* pageByName~[Seitenname]
* Beispiel: pageByName~pageHome

Seite anzeigen mit definierter Id
* pageById~[Id der Seite]
* pageById~1

Text eines Elements setzen
* setTextById~[Id des Feldes]~Text
* Beispiel: setTextById~1~Neuer Text des Feldes

Hintergrundfarbe eines Feldes setzen
* setBGColorById~[Id des Feldes]~Farb-Id
* Beispiel: setBGColorById~1~63488

Textfarbe eines Feldes setzen
* setFGColorById~[Id des Feldes]~Farb-Id
* Beispiel: setFGColorById~1~1024
