# Source: 1987 Engine & Emissions Diagnosis Manual (Manual H)

**Full title:** Ford 1987 Car Truck Light Medium Heavy Duty Engine & Emissions Diagnosis Shop Manual H  
**File:** `Full text of Engine Emissions Diagnosis.md`  
**Origin:** Archive.org OCR scan (djvu.txt), 1,147 pages  
**Coverage:** Engine and emissions diagnosis for all 1987 Ford car and truck models  
**Note:** This is a very large multi-vehicle manual. Information specific to the 5.0L EFI F-Series is in Parts I and II, with a focus on EEC-IV diagnostic procedures. OCR quality varies.

---

## Contents Summary

| Part | Topic |
|------|-------|
| I | Non-Electronic Systems |
| II | Electronic Systems (EEC-IV) |

**Part I sections:**
1. Emissions Control Identification/Application
2. Diagnostic Routines
3. Emissions Related Components
4. Carburetors, Fuel Charging Assemblies and Throttle Bodies
5. Catalyst and Exhaust Systems
6. Exhaust Gas Recirculation (EGR) Systems
7. Evaporative Emission Systems
8. Inlet Air Temperature Systems
9. Positive Crankcase Ventilation Systems
10. Thermactor Systems (Secondary Air Injection)
11. Fuel Delivery Systems
12. Glossary

**Part II:** Electronic Systems — EEC-IV Quick Test, fault code procedures (Section 16 referenced throughout)

---

## Key Facts Extracted

### Emissions Control Identification

- **Vehicle emission control information (VECI) decal location (F-Series, Ranger, Bronco with 5.0L):** Radiator support
- **Sample 5.0L VECI decal shown** (labeled as "typical"; calibration E5AE-9C485-CBD appears to be a 1985 calibration — the 1987 vehicle decal will differ):
  - Catalyst equipped
  - Spark plug: ASF-52G _(uncertain: from a sample 1985 calibration decal — verify against actual 1987 engine decal)_
  - Spark plug gap: 0.048–0.052" _(uncertain: same caveat as above)_
  - Application code shown: 5.0L-5FM

### Emission System Abbreviations

| Abbreviation | Meaning |
|--------------|---------|
| AIP | Air Injection (Thermactor) |
| BPA | Bypass Air |
| CFI | Central Fuel Injection |
| EFI | Electronic Fuel Injection |
| EGR | Exhaust Gas Recirculation |
| EGS | EGR (alternate) |
| HSC | High Swirl Combustion |
| PFE | Pressure Feedback Electronic EGR |
| SEFI | Sequential EFI |
| TFI | Thick Film Ignition |
| TK | Two-Way Catalyst |
| TWC | Three-Way Catalyst |

### Emissions Components (Section 3)

**Fuel Injector** (Part No. 9F593):
- Solenoid-operated valve; meters and atomizes fuel
- Opened/closed constant times per crank revolution; fuel amount controlled by pulse width
- Normally closed; operated by signal from ECA (EEC module)
- Note: High-pressure injectors can have high or low coil resistance; do not apply battery voltage directly

**Fuel Pressure Regulator** (Part No. 9C968):
- Attached to fuel supply manifold, upstream of injectors
- Diaphragm-operated relief valve
- One side exposed to fuel pressure; other side referenced to intake manifold vacuum (multi-point EFI)
- Spring preload sets nominal pressure
- Excess fuel returned to tank via return line

**Inertia Switch:**
- Used with electric fuel pump systems
- Opens on impact, shutting off fuel pump
- Must be manually reset (press button on top)
- **F-Series location:** Toe-board, to the right of the transmission hump
- Reset caution: Do not reset until complete fuel system inspected for leaks

**Heated Exhaust Gas Oxygen (HEGO) Sensor** (Part No. referenced in Section 3):
- Sends voltage signal to ECA indicating oxygen level in exhaust
- Location: In communicator tube connecting both exhaust pipes

### EEC-IV System (Section 16 / Part II)

The EEC-IV system controls: air/fuel ratio, ignition timing, EGR flow, Thermactor air flow, idle speed.

**EEC-IV Quick Test** (KOEO and KOER):
- KOEO = Key On Engine Off
- KOER = Key On Engine Running
- Self-test procedure referenced extensively; actual test steps and fault code tables are in Section 16 of this manual
- Diagnostic codes produced as numeric pulses

**EEC-IV fault codes** apply across car and truck 5.0L EFI applications; specific F-Series codes are in the 5.0L EFI section.

### Fuel System — EFI (Section 11 / Fuel Delivery)

**Fuel pressure specification (EFI running):** 35–45 psi (241–310 kPa)  
**Fuel pressure specification (key-off hold):** Should remain 35–45 psi for 60 seconds or longer after key-off  
_(Source: EEC-IV diagnostic procedure, applicable to 5.0L EFI)_

**Low fuel pressure causes cited:**
- Low fuel pump delivery
- In-tank filter restriction or kinked/leaking fuel hose

### EGR System

- EGR Valve Position (EVP) sensor monitors EGR valve position
- EGR Vacuum Regulator solenoid controlled by EEC-IV
- Thermactor (Secondary Air Injection) system: Air Bypass (TAB) and Air Diverter (TAD) solenoids

### Positive Crankcase Ventilation

- Closed-type PCV system on all gasoline engines
- PCV valve location (5.0L EFI): Rear of upper intake manifold

---

## Unresolved Questions from This Source

- [ ] Actual 1987 F-250 5.0L EFI calibration number — must be read from engine decal on rocker arm cover
- [ ] Actual spark plug part number and gap for 1987 calibration — not definitively stated; sample decal shows ASF-52G / .048–.052" but for a different calibration year
- [ ] Complete EEC-IV fault code list for 5.0L truck EFI — Section 16 content was not fully extracted
- [ ] Compression ratio — not found in this source

---

## Related Pages

- [Engine](../systems/engine.md)
- [Electrical](../systems/electrical.md)
- [Fuel System](../systems/fuel-system.md)
- [Common Issues](../problems/common-issues.md)
