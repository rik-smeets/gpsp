# gpSP for PowKiddy & Bittboy
An enhanced version of gpSP for PowKiddy and Bittboy devices. 

## How to install
*Note: in these instructions, it is presumed you use the [MiyooCFW](https://github.com/TriForceX/MiyooCFW/) custom firmware on your device.*
1. Download the latest release ZIP-file over at [Releases](https://github.com/rik-smeets/gpsp/releases/latest).
2. Copy the `gpsp_rumble.elf` file from the folder matching your device brand (i.e. PowKiddy or Bittboy).
3. Replace the existing `gpsp_rumble.elf` file in `main\emus\gpsp_rumble` with the downloaded version.

## Changelog
### v1.0
#### New features
- Map save/load state to buttons
- Auto save state feature (automatically save a state when exiting gpSP and open state when starting the emulator)
- Autofire A/B button (can be set in button mapping) ([based phantuanphong's solution](https://github.com/phantuanphong/gpsp-powkiddy))

#### Bugfixes
- Fix bug when loading or saving states didn't always use the displayed save slot
- Fix option to disable screen filter ([thanks to user @drowsnug on Discord](https://discord.com/channels/529983248114122762/540168599063756802/819836183105765406))
- Fix some minor text related issues in gpSP's GUI

#### PowKiddy specific changes
- Fix for A and B buttons being reversed in gpSP's GUI
- Fix mapping for A and B buttons being reversed

### pre v1.0
See [./readme.txt](./readme.txt)

## Thanks to
- gameblabla for writing the initial [Bittboy gpSP port](https://github.com/bittboy/gpsp)
- the other people mentioned in the changelog who shared improvements for gpSP