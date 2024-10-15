Step 1. Add the following lines to the end of gcode_macro.cfg on the printer:

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
