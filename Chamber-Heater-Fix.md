## Purpose
For excedingly large high-temp prints (greater than about 265mm), the chamber heater becomes obstructed by the print bed frame, potentially leading to thermal shutdown and subsequent print failure.  This code adds a macro to check the height of the bed and turns off the chamber heater before the obstruction prevents proper airflow.

## Directions
__Step 1.__ Add the following lines to the end of gcode_macro.cfg on the printer, found under the "Configuration" tab in the Fluidd interface:

```
[gcode_macro CHECK_CHAMBER_HEATER_Z]
gcode:
    {% if (printer.toolhead.position.z) > 265 %}
        M141 S0
    {% endif %}
```

__Step 2.__ Add the following line to the end of the "Layer change G-code" in your slicer, found in the printer profile:

```
CHECK_CHAMBER_HEATER_Z
```

## Acknowledgements
[Noisie Works](https://www.youtube.com/@NoizieWorks) and the unnamed Redditor who originally proposed this fix.  Thank you!
