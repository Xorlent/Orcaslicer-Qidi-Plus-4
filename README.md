# OrcaSlicer Qidi X-Plus 4 Profiles
OrcaSlicer printer profiles for the brand new Qidi Plus 4 FDM printer.  Profiles were adapted from the ones provided in the latest version of [QIDIStudio](https://github.com/QIDITECH/QIDIStudio), so should work fine.  These profiles have been tested on Qidi X 4 Plus firmware version 1.4.0 and OrcaSlicer 2.1.1.  
_Note: The beta version of OrcaSlicer may already have profiles for the X Plus 4 (per Qidi Github)_
> [!CAUTION]
> USE AT YOUR OWN RISK
> [!IMPORTANT]
> [Chamber Heater Fix Info and Instructions](https://github.com/Xorlent/Orcaslicer-Qidi-Plus-4/blob/main/Chamber-Heater-Fix.md)

## Installation
1. Close OrcaSlicer
2. Download and unzip the desired file from this repository
   - "Qidi X 4 Series Original.zip" gives you the stock Qidi profiles with only bug fixes applied
   - "Qidi X 4 Series Modified G-Code.zip" also gives you [improved printer profiles](#print_profiles)
   > TIP: In Windows, be sure to "Unblock" the ZIP before extracting (Right-Click->Properties)
3. Open the /resources/profiles folder
   - In MacOS, you need to "Show Package Contents" on the OrcaSlicer app
4. Paste the contents of this repo into the /profiles folder
   - No files should or will be overwritten in this process, leaving all Orcaslicer release files as-is
   - The final result should be:
     - A file called, "Qidi X 4 Series.json" in the /profiles folder
     - A subfolder called, "Qidi X 4 Series" in the /profiles folder
6. Launch OrcaSlicer and open the Add Printer dialog
   - Search for "X-Plus 4" and select the appropriate nozzle sizes
7. Connect to your printer using the Wi-Fi icon next to the printer name and enter the IP address of your device

## General Notes and Observations
### Generic Qidi filament profiles are included for PLA, PLA Silk, PETG, ABS, and TPU95A
- In my testing of their generic PETG profile, I recommend slowing all print speeds by 35-40% and increasing the flow ratio to .96 as a starting point
### Bed leveling
- The print bed on the unit I received is one of the truest 300+ mm original equipment plates I have measured, showing less than .22mm total runout and less than .15mm across all but one corner.
  - DO manually level the fully heated bed twice in succession before doing any other calibration for best results
<a id="print_profiles"></a>
### What do you mean by _improved printer profiles_ in "Qidi X 4 Series Modified G-Code.zip"?
  - Besides minor G-Code bug fixes included in the Original version, the G-Code has been updated to:
    - Give the build plate sufficient time to heat soak before calibration and printing
      - Currently set to 500000 ms (8 minutes and 20 seconds)
      - Case light turns off during the pre-heat
    -  Zero wait time between nozzle settle temperature and print start
    - Turn on the case light when the nozzle begins heating to start print
    - Turn off the case light when the print finishes

## License
QIDIStudio is licensed under the GNU Affero General Public License, version 3. QIDIStudio is based on BambuStudio by Bambu Lab.

BambuStudio is licensed under the GNU Affero General Public License, version 3. BambuStudio is based on PrusaSlicer by PrusaResearch.

PrusaSlicer is licensed under the GNU Affero General Public License, version 3. PrusaSlicer is owned by Prusa Research. PrusaSlicer is originally based on Slic3r by Alessandro Ranellucci.

Slic3r is licensed under the GNU Affero General Public License, version 3. Slic3r was created by Alessandro Ranellucci with the help of many other contributors.

The GNU Affero General Public License, version 3 ensures that if you use any part of this software in any way (even behind a web server), your software must be released under the same license.
