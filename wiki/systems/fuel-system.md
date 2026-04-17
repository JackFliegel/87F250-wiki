# Fuel System

**Summary:** Fuel delivery, injectors, fuel pump, pressure specs, and related notes for the 1987 F-250 5.0 EFI V8.

**Applicability:** 1987 Ford F-250, 5.0 EFI V8  
**Sources:**
- `Full text of Engine Shop Manual.md` (Sections 24-05, 24-35, 24-51)
- `Full text of Engine Emissions Diagnosis.md` (Sections 3, 11)
- `Full text of Electrical Vacuum Troubleshooting.md` (Section 40/54 — EEC component locations)

---

## Fuel Delivery Overview

The 5.0L EFI uses a multi-point, pulse-time fuel injection system managed by the EEC-IV module. Eight fuel injectors are mounted in the lower intake manifold, one per cylinder. Fuel is delivered by a **two-pump** electric system.

Source: Engine Shop Manual §24-05

---

## Fuel Pump System

| Item | Detail | Source |
|------|--------|--------|
| Pump configuration | **Two pumps** — low pressure (in-tank) + high pressure (chassis-mounted) | Engine Shop Manual §24-35 |
| Low pressure pump location | Inside fuel tank, inlet at bottom of internal sump | Engine Shop Manual §24-35 |
| High pressure pump location | Frame rail (chassis-mounted) | Engine Shop Manual §24-35 |
| High pressure pump output | 269.0 kPa (39 psi) working pressure; 60 L/hr (15.9 gal/hr) | Engine Shop Manual §24-35 |
| Overpressure relief | 850 kPa (123 psi) internal relief valve | Engine Shop Manual §24-35 |
| Fuel pump control | EEC-IV module via fuel pump relay | Engine Shop Manual §24-35 |
| Pump shutoff threshold | Engine below 120 rpm (or stopped) | Engine Shop Manual §24-35 |
| Key-on pre-pressurization | Pump runs ~1 second then shuts off if ignition not turned to START | Engine Shop Manual §24-35 |
| Fuel pump relay location | Under plastic shield at air cleaner support bracket | EVTM §40 |
| Inertia switch location (F-Series) | **Toe-board, to the right of the transmission hump** | Engine Shop Manual §24-35 |
| Inertia switch function | Opens on impact, cuts power to fuel pump | Engine Shop Manual §24-35 |
| Inertia switch reset | Press button on top of switch | Engine Shop Manual §24-35 |
| Fuel type required | Unleaded only (catalytic converter equipped) | Engine Shop Manual §24-01; Engine Emissions Diagnosis §1 |

**Warning:** Do not reset the inertia switch until the complete fuel system has been inspected for leaks.

---

## Fuel Pressure

| Condition | Spec | Source |
|-----------|------|--------|
| Engine running | 35–45 psi (241–310 kPa) | Engine Emissions Diagnosis §11 |
| Key-off hold (60 sec) | Should remain 35–45 psi | Engine Emissions Diagnosis §11 |
| High pressure pump working pressure | 39 psi (269 kPa) nominal | Engine Shop Manual §24-35 |

**Pressure regulator:** Part No. 9C968. Vacuum-referenced diaphragm type — one side sees fuel pressure, other side sees intake manifold vacuum. Maintains constant pressure differential across injectors. Mounted on fuel supply manifold upstream of injectors. Excess fuel returned to tank. Source: Engine Shop Manual §24-05; Engine Emissions Diagnosis §3

---

## Fuel Injectors

| Item | Detail | Source |
|------|--------|--------|
| Quantity | 8 | Engine Shop Manual §24-05 |
| Type | Solenoid-operated pintle and needle valve | Engine Shop Manual §24-05 |
| Part No. | 9F593 | Engine Emissions Diagnosis §3 |
| Mounting | Lower intake manifold, directed at intake valves | Engine Shop Manual §24-05 |
| Firing groups | Two banks of 4, fired alternately every crank revolution | Engine Shop Manual §24-05 |
| O-rings | Two per injector; inspect at removal | Engine Shop Manual §24-05 |
| Plastic hat (pintle cover) | Present on each injector; replace if missing or deteriorated | Engine Shop Manual §24-05 |

**Note:** High-pressure injectors can have high or low coil resistance. Do not apply battery voltage directly to injector terminals. Source: Engine Emissions Diagnosis §3

---

## Key Components

- **Fuel tank:** Location and capacity _pending_
- **Low pressure pump:** In-tank, internal sump, nylon inlet filter
- **High pressure pump:** Frame rail mounted; supplies main injection pressure
- **Fuel filter:** 20-micron inline filter, frame rail between high-pressure pump and engine. Arrow on filter body indicates flow direction — must point toward engine (pump → filter → engine). Source: Engine Shop Manual §24-51
- **Fuel supply manifold / fuel rail:** Part No. 9F792. Distributes fuel to all 8 injectors
- **Pressure regulator:** Part 9C968 — see above
- **Inertia switch:** Toe-board right of transmission hump — safety cutoff
- **EEC-IV module (ECA):** Behind LH kick panel — controls pump relay, injector pulse width

---

## Known Notes

- **Two-pump diagnosis:** When troubleshooting no-start or low fuel pressure, both pumps must be verified. The low-pressure pump feeds the high-pressure pump; a failed in-tank pump starves the chassis pump. Source: Engine Shop Manual §24-35
- **Pressure drop after key-off:** Normal to see some pressure drop; at cold temperatures the drop is faster (~20 psi drop in 5 seconds at 60°F). Source: Engine Emissions Diagnosis §11
- **Low pressure causes cited in manual:** Low pump delivery, restricted in-tank filter, kinked or leaking fuel hose. Source: Engine Emissions Diagnosis §11

---

## Unresolved Questions

- [ ] Fuel tank capacity and location (single or dual tank?) — check Section 24-50 or owner records
- [ ] Fuel filter part number (filter base assembly 9B072, tube assembly 9J338 referenced in Fig. 3 — confirm these are the correct 5.0L EFI part numbers)
- [ ] Fuel filter replacement interval — manual states "should last the life of the vehicle under normal driving conditions" but does not give a mileage spec (§24-51)
- [ ] Fuel pressure test port location — not explicitly described in extracted sections
- [ ] Low-pressure in-tank pump part number

---

## Related Pages

- [Engine](engine.md)
- [Electrical](electrical.md)
- [Common Issues](../problems/common-issues.md)
- [Fluids & Service](../maintenance/fluids-and-service.md)
- [Source: Engine Shop Manual](../sources/engine-shop-manual-1987.md)
- [Source: Engine Emissions Diagnosis](../sources/engine-emissions-diagnosis-1987.md)
