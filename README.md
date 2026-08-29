# Altium Designer PCB Design Rules & Stackup Templates

**elektroboard Altium Standard** is a reusable set of **Altium Designer PCB design rules (`.RUL`)** and **PCB layer stackup (`.stackup`) templates** for general-purpose **FR-4 PCB design**.

The repository provides a practical engineering baseline for:

- Altium Designer PCB design rules
- PCB clearance, track width and via rules
- 2-layer PCB stackup
- 4-layer PCB stackup
- 6-layer PCB stackup
- 1 oz outer copper / 0.5 oz inner copper multilayer designs
- Generic FR-4 PCB projects
- Reusable Altium PCB project setup

The files are manufacturer-independent starting templates. They are **not manufacturer-certified fabrication rules or controlled-impedance stackups**.

## ⚠️ Important Engineering Disclaimer

**Do not send a PCB to fabrication solely because these files import successfully or pass DRC.**

These rules and stackup templates are **generic engineering starting points only**. They are **not** a fabrication specification, manufacturer approval, controlled-impedance stackup, safety certification, or guarantee of manufacturability.

Before every fabrication order, the designer must independently verify at minimum:

- PCB manufacturer's current minimum/standard capabilities
- Copper thickness and finished copper requirements
- Finished board thickness and tolerance
- Core/prepreg construction and actual laminate availability
- Dielectric constant (Dk), loss tangent and impedance requirements
- Trace/space, drill, annular ring and via limitations
- Solder mask, silkscreen and board-edge requirements
- Creepage/clearance for the actual working voltage and environment
- Current-carrying capacity and thermal requirements
- Special process requirements such as HDI, microvias, via-in-pad or filled vias
- Assembly/DFM requirements for the selected PCB/PCBA manufacturer

**A passing Altium DRC does not prove that the PCB is manufacturable, electrically correct, safe, reliable, or compliant with any standard.**

The stackup files use nominal, generic FR-4 assumptions. For controlled impedance, RF, USB, Ethernet, PCIe, DDR or other high-speed interfaces, use the selected manufacturer's actual production stackup and impedance data.

The `.RUL` file may replace matching rules during import. Review all rule values, scopes and priorities after import. Project-specific rules always take precedence over these generic defaults.

Use of these files is entirely at the user's own engineering judgment and risk.

## Included

### PCB Rules
- `rules/ELEKTROBOARD_MASTER_RULES_v1.0.RUL`

### Generic Stackup Templates
- `stackups/ELEKTROBOARD_2L_1OZ_1.6MM.stackup`
- `stackups/ELEKTROBOARD_4L_1OZ-OUTER_0.5OZ-INNER_1.6MM.stackup`
- `stackups/ELEKTROBOARD_6L_1OZ-OUTER_0.5OZ-INNER_1.6MM.stackup`

## Design Philosophy

These files are intended as manufacturer-independent engineering starting points.

The stackups use generic FR-4 assumptions and are **not** controlled-impedance fabrication stackups.

For controlled-impedance interfaces such as USB, Ethernet, RF, DDR, PCIe, or similar high-speed designs, always obtain the selected PCB manufacturer's current production stackup and recalculate impedance using the actual dielectric and copper data.

## Generic Layer Functions

### 2 Layer
- L1: Signal / Components / Power
- L2: Preferably continuous GND where practical

### 4 Layer
- L1: Signal / Components
- L2: Solid GND
- L3: Power + low-speed signal
- L4: Signal

### 6 Layer
- L1: Signal / Components
- L2: Solid GND
- L3: Signal / Power
- L4: Signal / Power
- L5: Solid GND
- L6: Signal / Components

## Copper Assumptions

- 2L: 1 oz outer layers
- 4L: 1 oz outer / 0.5 oz inner
- 6L: 1 oz outer / 0.5 oz inner

## Important

Verify all design rules and stackup assumptions against your PCB manufacturer's current capabilities before fabrication.

Special cases should use project-specific rules and stackups:
- Controlled impedance
- RF
- High voltage
- High current
- 2 oz+ copper
- HDI / microvias
- Rigid-flex
- Safety-certified products




## What Is Included?

### Altium PCB Design Rules (`.RUL`)

The master `.RUL` file provides reusable Altium Designer rules for common PCB constraints including clearance, routing width, vias, annular ring, board-edge clearance, solder mask, silkscreen, polygon connections and routing behavior.

It also includes reusable routing-width classes for common signal categories such as signal, analog, I2C, SPI, RS485 and multiple power levels.

### Altium PCB Stackup Templates (`.stackup`)

Three generic FR-4 layer stack templates are included:

- 2-layer PCB — 1 oz copper
- 4-layer PCB — 1 oz outer / 0.5 oz inner copper
- 6-layer PCB — 1 oz outer / 0.5 oz inner copper

These templates are intended for normal PCB project setup, not controlled-impedance fabrication release.

## How to Import the Altium Design Rules

Open the target PCB project in Altium Designer and import:

`rules/ELEKTROBOARD_MASTER_RULES_v1.0.RUL`

When Altium asks how to handle existing rules, use:

`Add and replace matching rules`

After import, review all rule scopes, priorities and values before fabrication.

## How to Import an Altium Stackup File

Open the PCB document and go to:

`Design -> Layer Stack Manager`

Then use Altium Designer's stackup load/import command and select the appropriate `.stackup` file from the `stackups/` directory.

After loading the stackup, verify the copper layers, dielectric thicknesses, copper weights and total board-thickness assumptions against the selected PCB manufacturer's current production stackup.

## Typical Use Cases

This repository is intended as a starting point for general-purpose:

- Embedded electronics
- Microcontroller boards
- Industrial control PCBs
- Analog and mixed-signal boards
- RS485 / Modbus hardware
- Sensor interfaces
- Power distribution at ordinary PCB current levels
- Prototype and low/medium-complexity FR-4 PCB designs

Project-specific engineering is required for RF, controlled impedance, high voltage, high current, HDI, rigid-flex and safety-critical designs.

## FAQ

### Is this an official Altium Designer rule set?

No. This is an independent community engineering template for Altium Designer.

### Are these JLCPCB or PCBWay design rules?

No. The files are intentionally manufacturer-independent. They may be used as an engineering starting point, but every value must be checked against the selected PCB manufacturer's current capabilities before ordering.

### Does passing Altium DRC mean the PCB is manufacturable?

No. A clean DRC only indicates that the design satisfies the active Altium rules. It does not guarantee fabrication capability, electrical correctness, safety or standards compliance.

### Can I use these stackups for controlled impedance?

Not as a fabrication specification. Obtain the actual PCB manufacturer's stackup, dielectric data and impedance requirements first.

## Rule Import Summary

Use `Add and replace matching rules`, then verify all imported rule scopes, priorities and values before fabrication.
## Disclaimer and License

See [`DISCLAIMER.md`](DISCLAIMER.md) for the full engineering and liability disclaimer.

This repository is distributed under the MIT License. See [`LICENSE`](LICENSE).
