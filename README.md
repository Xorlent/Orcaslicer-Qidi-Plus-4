# OrcaSlicer Qidi X-Plus 4 Profiles
OrcaSlicer printer profiles for the brand new Qidi Plus 4 FDM printer.  Profiles were adapted from the ones provided in the latest version of [QIDIStudio](https://github.com/QIDITECH/QIDIStudio), so should work fine.  These profiles have been tested on Qidi X 4 Plus firmware version 1.4.0 and OrcaSlicer 2.1.1.
> [!CAUTION]
> USE AT YOUR OWN RISK

## Installation
1. Close OrcaSlicer
2. Download and unzip the file in this repository
   - In Windows, be sure to "Unblock" the ZIP before extracting (Right-Click->Properties)
3. Open the /resources/profiles folder
   - In MacOS, you need to "Show Package Contents" on the OrcaSlicer app
4. Paste the contents of this repo into the /profiles folder
   - No files should or will be overwritten in this process
   - The final result should be:
     - A file called, "Qidi X 4 Series.json" in the /profiles folder
     - A subfolder called, "Qidi X 4 Series" in the /profiles folder
6. Launch OrcaSlicer and open the Add Printer dialog
   - Search for "X-Plus 4" and select the appropriate nozzle sizes
7. Connect to your printer using the Wi-Fi icon next to the printer name and enter the IP address of your device

## General Notes and Observations
- Generic Qidi filament profiles are included for PLA, PLA Silk, PETG, ABS, and TPU95A
  - In my testing of their generic PETG profile, I recommend slowing all print speeds by 35-40% and increasing the flow ratio to .96 as a starting point
- The print bed on the unit I received is one of the truest original equipment plates I have measured
  - DO manually level the bed before doing any other calibration for best results
  - In the printer's Start G code, I recommend changing the line, "G4 3000" to "G4 500000" to give the large bed more time to heat soak

## License
QIDIStudio is licensed under the GNU Affero General Public License, version 3. QIDIStudio is based on BambuStudio by Bambu Lab.

BambuStudio is licensed under the GNU Affero General Public License, version 3. BambuStudio is based on PrusaSlicer by PrusaResearch.

PrusaSlicer is licensed under the GNU Affero General Public License, version 3. PrusaSlicer is owned by Prusa Research. PrusaSlicer is originally based on Slic3r by Alessandro Ranellucci.

Slic3r is licensed under the GNU Affero General Public License, version 3. Slic3r was created by Alessandro Ranellucci with the help of many other contributors.

The GNU Affero General Public License, version 3 ensures that if you use any part of this software in any way (even behind a web server), your software must be released under the same license.
