# DC-DC Boost Converter V1

A high-performance step-up DC-DC boost converter based on the **XL6009** switching regulator IC. Designed in KiCad.

[Circuit Design]

<img width="695" height="350" alt="top_image" src="https://github.com/user-attachments/assets/29a14a51-7f89-4c36-921d-f3fc63dadc3c" />
<img width="772" height="544" alt="circuit_design" src="https://github.com/user-attachments/assets/6c6bf03b-dd61-4deb-8423-1e820a760066" />



[PCB Top]

<img width="695" height="350" alt="top_image" src="https://github.com/user-attachments/assets/1eac766d-d43c-4c35-acfb-25ffd49c7a49" />


[PCB Bottom]

<img width="678" height="315" alt="Bottom_image" src="https://github.com/user-attachments/assets/dee2c0c3-4867-413c-ad44-cbe16c37e517" />

[PCB]

<img width="964" height="465" alt="pcb" src="https://github.com/user-attachments/assets/217639e1-3f48-4ad0-a2c6-b1d10061a6bf" />


## Features

- Wide input voltage range (XL6009: 5V–32V)
- Adjustable output voltage via 50K trimmer potentiometer
- 33µH switching inductor
- 40V/3A Schottky diode (SS34) for rectification
- Input and output filtering capacitors
- Compact PCB layout with pin header connectors

## Specifications

| Parameter          | Value            |
|--------------------|------------------|
| Controller IC      | XL6009 (XLSEMI)  |
| Topology           | Boost (Step-Up)  |
| Inductor           | 33µH             |
| Switching Diode    | SS34 (40V, 3A)   |
| Input Capacitor    | 47µF / 50V       |
| Output Capacitor   | 220µF / 50V      |
| Ceramic Caps       | 1µF (x2)         |
| Feedback Resistor  | 1KΩ              |
| Voltage Adjust     | 50K trim pot      |
| Input Connector    | J1 (+), J2 (GND) |
| Output Connector   | J3 (+), J4 (GND) |

## Schematic

The circuit uses the XL6009 in its standard boost configuration. The feedback pin (FB) is connected to a voltage divider formed by a 1K resistor and a 50K trimmer potentiometer, allowing the output voltage to be adjusted.

## Design Files

- **Schematic:** `Boost Converter V1.kicad_sch`
- **PCB Layout:** `Boost Converter V1.kicad_pcb`
- **Project File:** `Boost Converter V1.kicad_pro`

## Output Voltage Adjustment

The output voltage is set by the feedback divider:

```
Vout = 1.25V x (1 + RV1 / R1)
```

Where R1 = 1KΩ and RV1 is the 50K trim pot. This provides a wide adjustable range.

## Author

**Krishan CHOUDHARY** — 2025
