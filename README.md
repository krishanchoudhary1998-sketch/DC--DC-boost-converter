# DC--DC-boost-converter-PCB-

A high-performance step-up DC-DC boost converter based on the **XL6009** switching regulator IC. Designed in KiCad.

![Circuit Design](Docs/circuit_design.png)
![PCB Top](Docs/top_image.png)
![PCB Bottom](Docs/bottom_image.png)
![PCB](Docs/pcb.png)
 
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
