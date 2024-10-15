Step 1. Add the following lines to the end of gcode_macro.cfg on the printer, found under the "Configuration" tab in the Fluidd interface:

```
[gcode_macro CHECK_CHAMBER_HEATER_Z]
gcode:
    {% if (printer.toolhead.position.z) > 265 %}
        M141 S0
    {% endif %}
```

Step 2. Add the following line to the end of the "Layer change G-code" in your slicer, found in the printer profile:

```
CHECK_CHAMBER_HEATER_Z
```

Acknowledgements:  
[Noisie Works](https://www.youtube.com/@NoizieWorks) and the unnamed Redditor who originally proposed this fix.  Thank you!
