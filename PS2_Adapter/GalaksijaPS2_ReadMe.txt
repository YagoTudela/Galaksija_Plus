Galaksija Keyboard Adapter by PVV
PCB by RobertK (Retro Bertie), RetroBertie@outlook.com

Write either one of these images to EPROM D1 (27C512):
gal_keyb_adapter_rom_de.bin	(German keyboard layout)
gal_keyb_adapter_rom_en.bin	(English keyboard layout, still untested)
gal_keyb_adapter_PVV_1.bin 	(Russian keyboard layout)

And write main.HEX to D2 (PIC 16F628).

Thanks to hans61 at VzEkC for creating the German and English laoyut files. The German layout supports diagonal cursor keys movement on the numeric pad by pressing keys 1, 7, 9 or 3.


=== PCB History ===

Version 1.1a (2022-03-21)
- Outline with rounded corners added

Version 1.1 (2022-02-26)
- Connected X2 Pin 1 to Ground (Pin 1 of D1).
- Marked Pins 1 of X2 and X3

Version 1.0 (2021-09-21)
- Initial Release
