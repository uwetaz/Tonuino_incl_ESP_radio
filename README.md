# Tonuino_incl_ESP_radio
An Project which uses Tonuino and ESP32 based Web Radio in one unit with parallel HW parts

This repository contains information about an HW/SW extension to the classic Tonuino (https://tonuino.de/)

The extension is based on an parallel HW which is mainly based on an ESP32 dev board and VS1053 MP3 decoder. The parallel HW is selectable via Switch (Tonuino or Radio). The advantage ot the parallel system is for example the excellent
current consumption in Tonuino mode (60mA at 5V).

The first implemented function at the extension was an webradio based on the vs1053ext libary (https://github.com/schreibfaul1/ESP32-vs1053_ext).
Information about station and title is shown via an SSD1306 based OLED display. The 3 arcade buttons from Tonuino function have the same for radio mode and has the same function. Long press at up/down changes the station.
It is an really good and cheap alternative to raspberry pi based web radios (start up time until music plays 3s and power consumption on 5V 200mA).

The second function was to give the kids the chance to push speach messages to grandmas mobile via mail. This is for the kid only a "special" radio station where has to be entered via up/down). Record is started by hold pause button. If the kid release the spoken
message is send.
It is based on recording function (ogg-files to SD-card which is plugged at VS1053 board) which is possible via VS1053. For this I merged necessarry changes from https://github.com/adafruit/Adafruit_VS1053_Library to vs1053ext libary.
We have 5 of these Tonuino/ESP radio units at home (3 kids and each one form parents). On an 24hour powered raspberry pi (used for home automation) is an simple python script running which receives the ogg-file and sends to the relevant mail receiver.

It is planned to created with these setup an intercom system where we can send speach messages between Tonuino/ESP radio units in our family as an alternative to very bad walki talkis.

beside the described functions the FW it contains at the moment:
- FTP server
- WLAN FW update (OTA)
- telnet to give out wireless debug messages during development

19.01.2021
I have now prepared the information about the HW and provided some pictures. Until I can upload the ESP FW and the python script for the raspberry pi here I have to clean up the code. I'm not very experienced in coding. At this time point I have hard coded names and 
maildresses inside. So I have to spend some weeks or evenings more ;-).




