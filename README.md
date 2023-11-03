![](Yet%20another%20shitty%20carbon%20filter.jpg)

# Why yet another design?

I tried printing the famous [Nevermore Micro V6](https://github.com/nevermore3d/Nevermore_Micro), it ended up in frustration with parts that broke multiple times during assembly (jalousie) or did not fit (lid). I decided to design my own shitty carbon filter.

# Dimensions

I designed this air filter to be used standing up on the lower bottom side of my Voron V0, Voron Trident.

# Print and assembly instructions

Print in a material that withstands the temperature at which the filter will be used. I printed mine in ASA. No supports needed. If you have a color theme on your printer you may print the body in the base color and the mount and lid in the accent color.

Print one of the mounting brackets:

- `Yet another shitty carbon filter - 1515 mount.stl`
- `Yet another shitty carbon filter - 2020 mount.stl`

The 2 screw holes that connect to the extrusion will fit M3x8 (FHCS, BHCS, pan head). Use M3 t-nut or similar for in your aluminium extrusion.

Print `Yet another shitty carbon filter - body.stl`. You may want to use a brim if lifting is a problem. Slight lifting is not a problem.

Melt 2 heat set inserts M3x5x4mm into the holes they fit in:

![](Yet%20another%20shitty%20carbon%20filter%20-%20body%20-%20heat%20set%20insert%20locations.png)

Use a single M3x16 (up to M3x27) to screw the mount to the body:

![](Yet%20another%20shitty%20carbon%20filter%20-%20m3%20mount%20to%20body.png)

Print `Yet another shitty carbon filter - lid with 5015 fan.stl`.

Melt 2 heat set inserts M3x5x4mm into the holes they fit in:
![](Yet%20another%20shitty%20carbon%20filter%20-%20lid%20with%205015%20fan%20-%20heat%20set%20insert%20locations.png)

You can use 2 M3x8 (up to M3x65) screws to mount the lid to the body. Use 2 M3x20 (up to M3x22) to mount a 5015 blower fan to the lid.

# Electronics

Use your skills to connect the 5015 blower fan to whatever fitting power source. I used a 24V 5015 blower fan connected to my 3d-printer motherboard. I added an inline connector for easy disassembly. I then configured it in klipper as a `controller_fan` like this:

```ini
[controller_fan carbon_filter]
##  yet another shitty carbon filter - FAN3
pin: PD13
max_power: 1.0
shutdown_speed: 0.0
kick_start_time: 5.0
heater: extruder
fan_speed: 0.75
idle_timeout: 900
```

Customize `pin` to the real pin you use.

There is a slot in the lid to thread a ty-rap through, use it to add strain relief to for the wires to the fan:
![](Yet%20another%20shitty%20carbon%20filter%20-%20lid%20with%205015%20fan%20-%20ty-rap.png)

# Activated carbon

The ventilation holes at the air outlet on the body where designed to mostly contain 4mm activated carbon. The holes are 2mm higher than the bottom of the body so that carbon dust can settle there.

![](Yet%20another%20shitty%20carbon%20filter%20-%20body%20-%20air%20outlet.png)

I filled my shitty carbon filter with non-acidic activated 4mm carbon pellets that I ordered from a local aquarium store. Fill the filter body up to the top most inner supports, which is about 1cm from the top.

![](Yet%20another%20shitty%20carbon%20filter%20-%20body%20-%20filled%20with%20carbon.jpg)

I print mainly with ASA which smells bad during printing. When the shitty carbon filter is no longer able to remove the smell I replace the carbon pellets. The [Nevermore github repository](https://github.com/nevermore3d/Nevermore_Micro) has an interesting read about VOCs.

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)