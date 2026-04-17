# Engine — 5.0 EFI V8

**Summary:** Notes on the 1987 F-250's 5.0L (302 cu in) EFI V8 engine — specs, components, and sourced observations.

**Applicability:** 1987 Ford F-250, 5.0 EFI V8; also used in F-150 and Bronco  
**Transmission:** Unknown — to be confirmed from sources  
**Emissions:** Catalytic converter equipped (TWC); unleaded fuel required

**Sources:**
- `Full text of Engine Shop Manual.md` (1987 Light Truck Engine Shop Manual B, Section 21-21, 24-05, 23-01, 24-35)
- `Full text of Engine Emissions Diagnosis.md` (1987 Engine/Emissions Diagnosis Manual H, Section 3, 11)
- `Full text of Electrical Vacuum Troubleshooting.md` (1987 EVTM, Section 40/54)

---

## Specifications

| Item | Value | Source |
|------|-------|--------|
| Displacement | 302 cu in / 5.0L | Engine Shop Manual §21-21 |
| Configuration | OHV V-8 | Engine Shop Manual §21-21 |
| Bore × Stroke | 4.00" × 3.00" | Engine Shop Manual §21-21-39 |
| Firing order | **1-5-4-2-6-3-7-8** | Engine Shop Manual §21-21-39 |
| Oil pressure (hot @ 2000 rpm) | 275 kPa (40–60 psi) | Engine Shop Manual §21-21-39 |
| Fuel system | Multi-point EFI, 8 injectors | Engine Shop Manual §24-05 |
| Oil capacity (w/ filter) | 6 qt US / 5.6 L | Engine Shop Manual §21-01 |
| Oil capacity (w/o filter) | 5 qt US / 4.7 L | Engine Shop Manual §21-01 |
| Compression ratio | _pending — not found in OCR'd text_ | — |
| Horsepower | _pending_ | — |
| Torque | _pending_ | — |
| Coolant capacity | _pending_ | — |
| VIN position 8 code | Likely **N** _(uncertain — OCR table alignment)_ | Engine Shop Manual §20-00 |

---

## Engine Construction

| Feature | Detail | Source |
|---------|--------|--------|
| Block material | Special high-grade cast iron, thin-wall | Engine Shop Manual §21-21 |
| Crankshaft | 5 main bearings, precision-cast nodular iron | Engine Shop Manual §21-21 |
| Pistons | Aluminum alloy, tin plated | Engine Shop Manual §21-21 |
| Valve tappets | Hydraulic | Engine Shop Manual §21-21 |
| Rocker arms | Individually bolt-mounted (not shaft-mounted) | Engine Shop Manual §21-21 |
| Rocker arm lift ratio | 1.61:1 | Engine Shop Manual §21-21-39 |
| Combustion chamber volume | 60.6–63.6 cc | Engine Shop Manual §21-21-39 |
| Cylinder bore (std) | 4.0004–4.0052" | Engine Shop Manual §21-21-39 |
| Valve arrangement | I-E-I-E-I-E-I-E per bank (RT) | Engine Shop Manual §21-21-39 |

---

## Key Components

- **Intake manifold:** Two-piece aluminum casting (upper + lower); runner lengths tuned for torque/power. Source: Engine Shop Manual §24-05
- **Throttle body:** Air throttle body assembly; includes Throttle Position Sensor and Air Bypass Valve. Source: Engine Shop Manual §24-05
- **Fuel injectors (×8):** Solenoid-operated, pintle-type, individually mounted in lower intake manifold. See [Fuel System](fuel-system.md)
- **EGR system:** EGR valve with EVP sensor; EGR Vacuum Regulator solenoid controlled by EEC-IV. Source: EVTM §40; Engine Emissions Diagnosis
- **Ignition system:** TFI-IV with EEC-IV. Distributor uses Hall effect vane/PIP sensor. See [Electrical](electrical.md)
- **Timing:** Controlled entirely by EEC-IV; not a normal field adjustment on TFI-IV systems. Source: Engine Shop Manual §23-01
- **PCV valve:** Located at rear of upper intake manifold. Source: Engine Shop Manual §21-21
- **Engine identification decal:** On rocker arm cover — contains calibration number, build date, plant code, engine code. Source: Engine Shop Manual §21-21

---

## Ignition System Summary

| Item | Detail | Source |
|------|--------|--------|
| Ignition type | TFI-IV (Thick Film Integration IV) | Engine Shop Manual §23-01 |
| Engine management | EEC-IV | Engine Shop Manual §23-01 |
| Distributor trigger | Hall effect vane switch / PIP sensor | Engine Shop Manual §23-01 |
| Spark plug size | 14mm, ½" standard reach, tapered seat | Engine Shop Manual §23-01 |
| Spark plug (part) | ASF-52G shown in sample VECI decal — _uncertain, verify against actual 1987 decal_ | Engine Emissions Diagnosis §1 |
| Spark plug gap | 0.048–0.052" shown in sample VECI decal — _uncertain, verify against actual 1987 decal_ | Engine Emissions Diagnosis §1 |
| Timing adjustment | Not a normal adjustment; EEC-IV controlled | Engine Shop Manual §23-01 |

---

## Known Notes

- **Two-pump fuel system:** The 5.0L EFI uses a low-pressure in-tank pump plus a separate high-pressure chassis-mounted pump. This is important for diagnosis — both must work. Source: Engine Shop Manual §24-35
- **Aluminum intake manifold:** Unlike the 5.8L which uses cast iron, the 5.0L EFI uses an aluminum intake manifold. Source: Engine Shop Manual §21-21
- **Unleaded fuel only:** Catalytic converter equipped. "Unleaded Fuel Only" label required near filler and on instrument cluster. Source: Engine Shop Manual §24-01

---

## Unresolved Questions

- [ ] Confirm VIN position 8 engine code letter (likely N) — verify against actual vehicle VIN
- [ ] Compression ratio — not extracted from OCR'd manuals; check engine decal or separate spec bulletin
- [ ] Horsepower and torque ratings — not in shop manual; may be in a spec bulletin or the emissions facts book
- [ ] Coolant system capacity — not extracted; likely in cooling system section (Group 27)
- [ ] Confirm 49-state vs. California emissions calibration — check actual engine decal calibration number
- [ ] Transmission type (automatic/manual, model number) — confirm from vehicle

---

## Related Pages

- [Electrical](electrical.md)
- [Fuel System](fuel-system.md)
- [Fluids & Service](../maintenance/fluids-and-service.md)
- [Common Issues](../problems/common-issues.md)
- [Source: Engine Shop Manual](../sources/engine-shop-manual-1987.md)
- [Source: Engine Emissions Diagnosis](../sources/engine-emissions-diagnosis-1987.md)
- [Source: EVTM](../sources/electrical-vacuum-troubleshooting-1987.md)
