---
title: STM32 BluePill
author: Maik
layout: post
---

Ich habe einen STM32-Klon, auch BluePill genannt. Es hat mich (mal wieder) etwas Aufwand gekostet, um den Bootloader wieder richtig zu flashen. Damit das nicht noch einmal passiert, halte ich hier fest, wie ich das getan habe.

Dazu habe ich mir erst die Binary-File von rogerclarkmelbourne besorgt. *Vorsicht:* Die aktuellste Version funktioniert mit dem STM32F103C nicht.

Zum Hochladen des Bootloaders muss das Arduino-STM32 Projekt von rogerclarkmelbourne heruntergeladen werden und installiert werden. Die Doku von ihm reicht hier aus. 

Dann muss der STM32 an einen Serial-to-USB-Adapter angeschlossen werden und mit stm32flash geflasht werden. BOOT0 muss auf HIGH gesetzt werden.

Danach ist der STM32 bereit zum Upload. Beim Start des Upload-Vorgangs lädt pulsiert PC13 um anzuzeigen, dass ein manueller RESET notwendig ist. Den sollte man nicht verpassen, dann startet der Download auf den STM32. 

* https://github.com/rogerclarkmelbourne/Arduino_STM32/wiki/Flashing-Bootloader-for-BluePill-Boards
* https://medium.com/@paramaggarwal/programming-an-stm32f103-board-using-usb-port-blue-pill-953cec0dbc86