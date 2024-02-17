# Galaksija_Plus
 GalaksijaPlus

Galaksija Plus Replica by Fifan/PVV: Assembly Guide 
by RobertK a.k.a. Retro Bertie (2022)
RetroBertie@outlook.com

https://drive.google.com/drive/folders/1J3synVV-5PiKcZs9oFsY-6CqWDRKv7X2

This is a replica of the Z80-based "Galaskija Plus" DIY computer from Yugoslavia from the 1980s.

The original files had been published on...

http://www.spetsialist-mx.ru/Galaksija/index6.html

...but this web site is no longer available, so I have put all the files online here and added a BOM, and the Gerber and Sprint Layout files for my PS/2 keyboard adapter PCB.

GalaksijaPlus_Fifan_Schematic.pdf			Scheme of Galaksija Plus clone from Fifan
galaksija_chrgen.rar					Binary file for EPROM 27C64 "CHRGEN" (DD5)
galaksija_rom_v8_6.zip					Binary file for EPROM 27C128 "ROM" (DD11)
GalaksijaPlusGerbers.rar				Gerber files for the production of PCB
PVVSDcard.rar						File archive for SD card from PVV
PVVPS2adapter.zip					File archive for PS/2 keyboard adapter from PVV
GalaksijaPlus_PVV_BOM.xls				BOM for the main board, PS/2 adapter and Sound Generator (Retro Bertie)
GalaksijaPlusClone_BoardComplete_RetroBertie.jpg	Photo of the complete board (Retro Bertie)
GalaksijaPlusClone_BoardEmpty_YT2FSG.jpg		Photo of the empty board (YT2FSG)

For writing the 27C64 EPROM DD5 ("CHRGEN"), use the file GALAXY_CHRGENP8.BIN (8K).
For the 27C128 EPROM DD11 ("ROM") use GALAXY_ROM16.BIN (16K).

The following modifications should be done (they are already included in the BOM):

1. Video Output
Video Components are: VT2, R16, R17, C19, C20
R16 = 0 (connect directly)
R17 = 220R
C19 = 4.7uF
Do not mount C20

2. SD Card
Instead of VD4 and VD5, use a 78L33 (3.3V) voltage stabilizer
Left Pin = Input, Centre Pin = GND, Right pin = Output

3. Power Supply for the Main Board
It is recommended to use a laboratory PSU, start at 5V and reduce the voltage until the picture gets stable.
The picture should get stable when the voltage is reduced to 4.35 Volts.
If you don't have a laboratory PSU, you can use a 5V mobile phone charger, reduce the voltage using a 1N4007 diode. If the resulting voltage should be too low, use two Schottky diodes (e.g. 1N5817 or 1N5819) instead.
Connect XP2 Pin 1 (the rightmost pin) with DD14 Pin 8 (GND), this will connect ground between the main board and the PS/2 adapter. With this modification, the keyboard will work with separate power supplies too.

4. The correct values for the resistors R11 and R14 are:
R11 100
R14 2,4K
In the schematic, their values are swapped, with the result that loading from the audio input would not work.


Here is a Youtube video showing my building process:
https://youtu.be/Uxc2ua1hdcY


=== SOURCES / REFERENCES ===

http://www.spetsialist-mx.ru/Galaksija/
The repository for the main board Gerber files, ROM images and Schematic. Now offline, an archived version can be accessed here:
https://web.archive.org/web/20210123223417/http://www.spetsialist-mx.ru/Galaksija/index6.html

http://emulator.galaksija.org/MagScans/index.html
The magazine scans shown in the beginning of my video were downloaded from there.

https://www.youtube.com/watch?v=NPDcvZwGBMA&t=24s
Youtube video "Voja Antonic o igrama na Galaksiji", the photo of Mr. Antonic was taken from there.

https://www.qsl.net/yt2fsg/galaksija/galaksija_clone.html
Goran's Galaksija Clone, the photo of the empty board was taken from there.


=== OTHER LINKS ===

http://retrospec.sgn.net/users/tomcat/yu/Galaksija_list.php
Software Archive

http://galaksija.epizy.com/Help/Tape/
Another software Archive on galaksija.epizy.com

https://github.com/z88dk/z88dk/wiki/Platform---Galaksija
z88dk C compiler supporting the Galaksija system (among many other machines)

https://blog.vladovince.com/building-a-galaksija-the-1980s-yugoslav-8-bit-microcomputer-part-i-the-tech/
https://github.com/mejs/galaksija
Building the original Galaksija computer

https://oldcomputer.info/8bit/galaksija/index.htm
Another person who has built the original Galaksija

https://www.apuliaretrocomputing.it/wordpress/?p=4234
One more original Galaksija built

