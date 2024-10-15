Add the following lines to the end of gcode_macro.cfg on the printer:

```
[gcode_macro CHECK_CHAMBER_HEATER_Z]
gcode:
    {% if (printer.toolhead.position.z) > 265 %}
        M141 S0
    {% endif %}
```
