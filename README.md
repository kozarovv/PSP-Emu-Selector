PSP Emu Selector
==========================

Application for changing psp_emulator file versions on firmware 4.81, 4.82 (CEX, DEX, DECR (decr untested)). 
Based on modified version of **XMB Manager Plus (XMBM+) Installer.**
For original installer readme check file "READMEinstaller.markdown" 

## Usage

Install pkg file. Open application, and follow onscreen instuctions.

## Available options

- USE ENCRYPTED MINIS2.EDAT - Clean emulator without additional features. Only standard cobra patches are applied.
- USE DECRYPTED MINIS2.EDAT - Custom emulator version with patches by mysis to allow decrypted minis2.txt to be read.

Work only on 4.81, 4.82 cobra and non cobra firmware. App is changing files on dev_flash!

## Changes from Installer to Selector

- Obviously renamed project
- Removed reboot prompt for devflash operations (not needed for netemu change) 
- Fixed string centering in menus (ugly hack)
- Graphical changes (strings, colors, target names, etc.)
- Changed usleep values for buttons 
- Changed way of naming backups folder.
- Removed some refers to variable names in dialogs. Specially app_choice ones.
- More that I forgot, anyway source is here 
- Only backup of last used emu is created. Old backup is overwritten with new.
- require noRSX 0.29 to build
- Added scetool flags to makefile

## Build

- Install NoRSX library in version 0.29 (no earlier, no later): https://github.com/wargio/NoRSX/tree/a0d1d0c6c47561df70813fcf86df610d982ffbfc
- Other requirements are the same like in original installer code (PSl1GHT, etc.). But require custom psp_emulator.self files to be added, and empty.txt to be removed, before pkg compilation.

## Credits

- andreus, and XMBM+ Team for great installer
- mysis for r.e. and patches to psp_emulator
- deroad for noRSX

Visit Git (Installer): https://github.com/XMB-Manager-Plus/xmb-manager-plus-installer
