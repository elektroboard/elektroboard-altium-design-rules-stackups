# Disclaimer

## Engineering Use Only

The files in this repository are provided as generic engineering reference material and starting templates for Altium Designer.

They are not:

- a PCB fabrication specification,
- a manufacturer's approved design-rule set,
- a guaranteed manufacturable stackup,
- a controlled-impedance design,
- a safety certification,
- a compliance statement,
- or a substitute for professional engineering review.

## Mandatory Verification Before Fabrication

The user/designer is responsible for verifying all design rules and stackup parameters against the selected PCB manufacturer's latest published capabilities and the actual requirements of the project before placing any fabrication or assembly order.

This includes, without limitation:

- trace width and spacing,
- copper thickness,
- drill and via geometry,
- annular ring,
- solder mask and silkscreen limits,
- board-edge clearance,
- finished board thickness,
- available core/prepreg constructions,
- laminate material properties,
- dielectric constant and loss tangent,
- impedance requirements,
- creepage and clearance,
- current carrying capacity,
- thermal performance,
- assembly constraints,
- and any relevant regulatory or safety requirements.

## Stackup Limitation

The included stackup files use nominal generic FR-4 values for convenience.

They are not intended to prescribe the actual material construction a PCB manufacturer must use.

For controlled impedance or high-speed designs, including RF, USB, Ethernet, PCIe, DDR and similar interfaces, obtain the selected manufacturer's current production stackup and impedance requirements before final routing and fabrication.

## DRC Limitation

A design that passes Altium Designer DRC using these rules is not necessarily manufacturable, electrically correct, reliable, safe, or compliant with any applicable standard.

Rule import can also change or replace existing project rules. The user must review rule scopes, priorities and values after import.

## High-Risk / Special Applications

These generic templates should not be used without project-specific engineering review for applications involving, among others:

- mains or hazardous voltages,
- reinforced or functional insulation,
- high current,
- 2 oz or heavier copper,
- controlled impedance,
- RF,
- HDI or microvias,
- via-in-pad,
- rigid-flex,
- medical,
- automotive functional safety,
- aerospace,
- life-support,
- fire-safety,
- or other safety-critical applications.

## No Warranty

THE FILES AND INFORMATION IN THIS REPOSITORY ARE PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, NON-INFRINGEMENT, MANUFACTURABILITY, ELECTRICAL PERFORMANCE, RELIABILITY, OR COMPLIANCE.

TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, THE AUTHORS AND CONTRIBUTORS SHALL NOT BE LIABLE FOR ANY CLAIM, DAMAGES, LOSSES, COSTS, PRODUCTION ERRORS, SCRAP, REWORK, DELAYS, OR OTHER LIABILITY ARISING FROM OR RELATED TO THE USE OF THESE FILES OR INFORMATION.

By using these files, you acknowledge that final design verification and release to manufacturing remain your responsibility.

---

This disclaimer is an engineering/publication safeguard and is not legal advice. Legal effect can vary by jurisdiction.
