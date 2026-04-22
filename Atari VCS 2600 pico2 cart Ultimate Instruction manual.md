UNOCART-2600
Instruction Manual
Revision 1.4 21/3/2018
Atari 2600 SD multi-cart
1
Quick Start
The UnoCart -2600 is an Atari cartridge emulator. It supports cartridges with up to 64k of ROM and 32k of RAM.
First, copy BIN, ROM or A26 files to an SD card and insert it into the cartridge. Check the TV configuration jumper on
the back of the board matches your TV system. Insert the cartridge in the Atari 2600. If the board is uncased, check
you’ve got it the right way round (see picture). Power on the Atari and use the joystick to choose an item and the
fire button to start it.
PAL/NTSC Configuration
The jumper on the back of the board allows you to select whether the cartridge uses NTSC or PAL/PAL60 for the
built-in menu. You can remove the jumper completely if you are using a NTSC TV.
Note that this jumper only applies to the cartridge menu (and also to the Supercharger BIOS if you are using a
Supercharger cartridge type). Once you select a ROM to emulate, the TV picture produced will be entirely
dependent on the cartridge being emulated. In general there were separate PAL and NTSC versions of each
cartridge – make sure you get the correct version.
SD Cards
SD cards should be formatted as FAT32. Newer SD cards may come formatted as exFAT. These can be used with the
UnoCart-2600, but need to be re-formatted as FAT32 on your computer prior to use. Note that the UnoCart-2600
firmware will only show up to 80 items per directory. You can use directories to organise your files.
2
Menu
The menu allows you to navigate the files on the card and select a title to use. Joystick up and down will move
through the items one at a time. You can also use joystick left and right to move to the previous or next page. Press
fire to select an item. You can also use the SELECT button on the console to move to the next item, and RESET to
select an item, if you don’t have a joystick plugged in.
Compatibility
The UnoCart-2600 should be able to emulate every cartridge released during the commercial life of the 2600.
Newer homebrew titles should also be compatible with the UnoCart-2600, unless they use the DPC+ co-processor
features specific to the Harmony/Melody cartridge. Note that the DPC support on the cartridge is not complete but
it is sufficient to play Pitfall II.
Arcadia/Starpath Supercharger titles are emulated with the multi-load parts combined in a single file. Up to 256
loads are supported (2MB file). The Supercharger BIOS will use the TV type set by the UnoCart-2600 TV jumper.
ROM Files
The UnoCart uses cartridge detection signatures from the Stella Atari 2600 emulator to auto-detect all common
cartridge types. If a file has an extension of .BIN, .ROM or .A26 it will be auto-detected. If you want to force the
cartridge to be emulated as a specific type, you can use the file extensions listed in the table below.
Cartridge Type ROM RAM File Extension
2K 2K .2K
4K 4K .4K
F8 8K .F8
F8 SC 8K 128 bytes .F8S
F6 16K .F6
F6 SC 16K 128 bytes .F6S
F4 32K .F4
F4 SC 32K 128 bytes .F4S
FE (Activision) 8K .FE
3F (Tigervision) <=64K .3F
3E <=64K <=32K .3E
E0 (Parker Bros) 8K .E0
0840 8K .084
CV (CommaVid) 2K 1K .CV
EF 64K .EF
EF SC 64K 128 bytes .EFS
F0 64K .F0
FA (CBS RAM Plus) 12K 256 bytes .FA
E7 (M-Network) 16K 2K .E7
DPC (Pitfall II) 8K+2K .DPC
Supercharger 256 loads .AR
3
Firmware re-programming (advanced)
The board can be re-programmed using an ST-Link device. The programming header is at the top of the board. First
connect the 3 pins to the equivalent pins on your ST-Link. You should then connect the ST-Link device to the USB
port of your computer. You will also need to power the board – the easiest way to do this is to plug the board into
your Atari 2600 and power on. The ST-Link software should then be able to connect to the STM32F407 and reprogram
the firmware.
The latest firmware is available on the project website: https://github.com/robinhedwards/UnoCart-2600
Pin SWD Function
1 SWDIO SWD I/O
2 GND GND
3 SWCLK SWD Clock
Microcontroller (advanced)
The UnoCart-2600 will be fitted with either a STM32F407VGT6 (1meg flash) or a STM32F407VET6 (512k flash)
microcontroller. Please refer to your PCB to determine which one is present on your device. If you are developing
new firmware for the cartridge, the table below shows the pins connected to the cartridge port & micro SD card slot.
STM32 Pin(s) Cartridge Port STM32 Pin(s) Function
PD0...12 A0…A12 PB5 MicroSD CS
PE8…15 D0…D7 PB13 (SPI2,2) MicroSD CLK
PC0 TV Jumper PB14 (SPI2,2) MicroSD DO
PC1 TV Jumper PB15 (SPI2,2) MicroSD DI
Credits
Original idea, hardware and firmware by Robin Edwards (electrotrains at atariage).
Additional cartridge support and firmware additions by Christian Speckner (DirtyHairy at atariage
