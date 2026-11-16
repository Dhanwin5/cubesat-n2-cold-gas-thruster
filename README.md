# 3U CubeSat Nitrogen Cold Gas Propulsion - Fabrication Package

**Author: Dhanwin Mehta** · © 2026 Dhanwin Mehta. All rights reserved.

> [!WARNING]
> **PRELIMINARY - NOT RELEASED FOR MANUFACTURE.**
> This package describes a 300 bar pressure vessel. It has known open issues, including a tank
> safety factor below the stated requirement when specification-minimum material properties are used.
> Do not build, pressurise or test any part of it. Nothing here has been reviewed or signed off by a
> qualified pressure-systems engineer. The engineering review checklist in the detail engineering
> report has 19 open items.

## What this is

The nitrogen option from Part 1 of my LinkedIn series *Beyond Specific Impulse*, taken from a
sizing study to a fabrication package: drawings, bill of materials, electrical schematics, method
statement, operating procedure, risk analysis, CAD models and CFD of the nozzle.

| Design basis | Value |
| --- | --- |
| Spacecraft | 3U CubeSat, 4 kg wet, 20 m/s delta-v |
| Propellant | Nitrogen, 117.0 g, 300 bar at 20 °C |
| Tank | Al 6061-T6, ID 60 mm, wall 7.5 mm, OD 75 mm, two halves EB welded and re-heat-treated |
| Thruster | Conical nozzle, throat 0.280 mm, exit 0.911 mm, area ratio 10.58 |
| Performance (laminar CFD) | 46.5 mN, Isp 70.6 s vacuum, discharge coefficient about 0.94 |

## Contents

| Folder | Document | What it contains |
| --- | --- | --- |
| [`01_drawings`](01_drawings) | Fabrication drawings, Rev B | 10 sheets: tank half, tank weldment, nozzle insert, nozzle housing, clamp, valve tray, thruster plate, plumbing lines, assembly layout, exploded view with torques. ASME Y14.5-2018, third angle, mm |
| [`02_electrical`](02_electrical) | Electrical schematics, Rev B | 3 sheets: block diagram and inhibits, valve drivers and sensor circuits, connector pin tables and power budget |
| [`03_engineering_report`](03_engineering_report) | Detail engineering report, Rev C | Decisions, rechecked numbers, stress margins, test plan, review checklist, open assumptions, launch-provider requirements |
| [`04_bill_of_materials`](04_bill_of_materials) | Bill of materials, Rev C | 49 line items with part numbers, materials, masses and datasheet links (Excel) |
| [`05_method_statement`](05_method_statement) | Method statement, Rev A | Build sequence with hold points, hazards and controls, detailed methods |
| [`06_operating_procedure`](06_operating_procedure) | Standard operating procedure, Rev A | Red lines, loading, test firing, on-orbit burns, safing, contingencies |
| [`07_risk_analysis`](07_risk_analysis) | Risk analysis, Rev A | 28-item risk register and 27-line FMEA (Excel) |
| [`08_cad_step`](08_cad_step) | CAD models, Rev B | 15 manufactured parts and the assembly as STEP files |
| [`09_cfd`](09_cfd) | CFD of the nozzle | AeroFlowSim reports (PDF and HTML) for medium Euler, fine Euler grid study and laminar runs, plus plots |

PDFs and images preview in the browser. Excel, STEP and HTML files open after download
(open the HTML reports in a web browser).

## Key findings

- **Discharge coefficient about 0.94, not 1.0.** Thrust and mass flow are about 6 to 7 % below the
  quasi-1D design values. The flow acceptance test on drawing PT-3U-N2-303 cannot be met as written.
- **Tank safety factor:** 2.02 on peak hoop stress with typical properties, 1.66 on von Mises with
  specification minimums. Open decision.
- **Mass:** propulsion is about 54 % of the 4 kg spacecraft.
- **Launch acceptance:** a 300 bar vessel will need a waiver from most dispenser providers.

## How it was made

The documents were produced working with Claude (Anthropic) as an AI assistant; I set the design basis
and made the engineering decisions. The CFD was run in [AeroFlowSim](https://github.com/Dhanwin5/AeroFlowSim),
my own 2D solver. Each document states that it was produced with AI assistance.

## Copyright

© 2026 Dhanwin Mehta. All rights reserved. You may view and download these files for reference.
Reproduction, modification or redistribution requires written permission from the author.
