# Source: 1987 Electrical & Vacuum Troubleshooting Manual (EVTM)

**Full title:** Ford 1987 Bronco F-150 F-250 F-350 Electrical & Vacuum Troubleshooting Shop Manual  
**File:** `Full text of Electrical Vacuum Troubleshooting.md`  
**Origin:** Archive.org OCR scan (djvu.txt), 151 pages  
**Coverage:** All electrical circuits and vacuum systems for 1987 Bronco, F-150, F-250, F-350  
**Note:** This is the EVTM — wiring diagrams with troubleshooting hints, not step-by-step repair procedures. OCR quality for diagram labels is variable.

---

## Contents Summary

| Section | Topic |
|---------|-------|
| 1 | How to Use This Manual |
| 2–3 | How to Find the Electrical Problem |
| 4 | Electrical Symbols |
| 5 | Grounds |
| 15–19 | Fuse Panel / Circuit Protection |
| 18–19 | Power Distribution (Gasoline) |
| 22–24 | Power Distribution (Diesel) |
| 27 | Ignition |
| 30 | Start (Gasoline) |
| 39 | Start/Ignition (EEC) (4.9L and 5.0L) |
| 40 | Electronic Engine Control (EFI 5.0L) |
| 45 | Carburetor Circuits |
| 46 | Charge (Gasoline) |
| 49 | Electronic Engine Control (EEC) |
| 54 | Electronic Engine Control (EFI 5.0L) — repeated section |
| 62–80 | Lamps (exterior, interior, instrument) |
| 81 | Anti-Lock Brakes |
| 83 | Brake Warning Indicator |
| 89 | Electronic Shift — 4 Wheel Drive |
| 92 | Fuel Tank Selector/Gages (Gasoline) |
| 93 | Coolant Temperature Gage |
| 96 | Tachometer |
| 101 | Electric Fuel Pump Control |
| 106 | Horn; Cigar Lighter |
| 108 | Windshield Wiper/Washer |
| 113 | Power Windows |
| 116 | Tailgate Power Window; Rear Window Defrost |
| 120 | Power Door Locks |
| 123–124 | Radio |
| 125 | Trailer |
| 127 | Vacuum Symbols |
| 128 | Vacuum Distribution |
| 129 | How to Find the Vacuum Problem |
| 130 | Speed Control |
| 134–135 | Heater; A/C-Heater |
| 142–148 | Component Testing (switches, etc.) |

---

## Key Facts Extracted

### Fuse Panel — Gasoline (F-150–F-350, page 19)

The fuse panel is dash-mounted. Fuse color codes: 4A=Pink, 5A=Tan, 10A=Red, 15A=Lt Blue, 20A=Yellow, 25A=Natural, 30A=Lt Green.

| Position | Amps | Circuits Protected |
|----------|------|--------------------|
| 1 | 15 | Turn/Stop/Hazard Lamps; Speed Control |
| 2 | — | Not used |
| 3 | — | Not used |
| 4 | 15 | Exterior Lamps; Instrument Illumination |
| 5 | 15 | Turn Lamps; Backup Lamps; Rear Window Defrost |
| 6 | 15 | Speed Control; Electronic Shift–4 Wheel Drive |
| 7 | — | Not used |
| 8 | 15 | Courtesy, Dome, Cargo Lamps; Warning Buzzer |
| 9 | 30 | Heater; A/C-Heater |
| 10 | 20 | Anti-lock Brakes |
| 11 | 15 | Radio; Main Light Switch; Clock Illumination |
| 12 | 25 / 30 cb | Tailgate Power Window; Power Mirrors / Power Door Locks; Electronic Shift–4WD |
| 13 | — | Not used |
| 14 | 25 / 30 cb | Tailgate Power Window / Power Windows |
| 15 | 10 | Auxiliary Fuel Tank Selector |
| 16 | 30 | Horn; Cigar Lighter; Speed Control; 4.9L EFI After Run Blower |
| 17 | 5 | Instrument Illumination; Clock Dimming |
| 18 | 15 | Seatbelt Buzzer; Warning Indicators; Carburetor Circuits; Tachometer; Diesel Glow Plug Control; Diesel Indicators; Electric Fuel Pump Control (7.5L only) |

**Always-hot fuses:** 1, 4, 8, 12, and others — powered regardless of ignition position.

### Power Distribution

- Alternator and Battery connected at Starter Relay hot terminal
- High-current circuits protected by fuse links (not panel fuses)
- Low-power circuits protected by fuse panel fuses

### EEC-IV System (5.0L EFI) — Component Locations

The Electronic Engine Control Assembly (ECA/EEC module) is located **behind the LH (left-hand/driver side) kick panel**.

| Component | Location (5.0L EFI) |
|-----------|---------------------|
| Air Charge Temperature (ACT) Sensor | #6 lower intake manifold runner |
| Engine Coolant Temperature (ECT) Sensor | At intake manifold heater hose elbow |
| EGR Vacuum Regulator Solenoid | On bracket on intake manifold |
| EGR Valve Position (EVP) Sensor | At EGR valve on intake manifold |
| Knock Sensor (KS) | In cylinder block behind the intake manifold |
| Manifold Absolute Pressure (MAP) Sensor | On bracket on intake manifold |
| Thermactor Air Bypass (TAB) Solenoid | On bracket on intake manifold |
| Thermactor Air Diverter (TAD) Solenoid | On bracket on intake manifold |
| Throttle Air Bypass Valve Solenoid | On throttle body |
| Throttle Position Sensor (TPS) | Connected to throttle body shaft |
| Heated Exhaust Gas Oxygen (HEGO) Sensor | In communicator tube connecting both exhaust pipes |
| EEC Power Relay | Under plastic shield at air cleaner support bracket |
| Fuel Pump Relay | Under plastic shield at air cleaner support bracket |
| Vehicle Speed Sensor (VSS) | At transmission |
| VIP Self-Test Connector | See EEC wiring diagram (page 40/54) |
| ECC Clutch Switch | Above clutch pedal |

### EEC-IV System Description (5.0L EFI)

The ECA optimizes tailpipe emissions, fuel economy, driveability, and performance by receiving sensor inputs and sending control signals to:
- Fuel injectors (air/fuel ratio)
- Ignition timing (via TFI module SPOUT signal)
- EGR flow
- Thermactor air flow
- Idle speed (via Throttle Air Bypass Valve)

**System inputs (sensors):** PIP, TPS, ECT, HEGO, MAP, Knock Sensor, Power Steering Pressure Switch, ACT

**Power steering pressure switch:** Signals ECA to raise idle speed when PS load increases.

### Grounds

- Engine grounds G801 and G802 apply to **both 4.9L and 5.0L gasoline engines**
- Refer to page 5 (Grounds section) for locations

---

## Unresolved Questions from This Source

- [ ] Exact location of fuse panel (under dash? exact position) — diagram referenced but OCR of diagrams is partial
- [ ] VIP Self-Test Connector physical location — noted in wiring diagram but not textually described in legible OCR
- [ ] Knock sensor — listed as "in cylinder block behind the intake manifold" but precise cylinder location unclear (4.9L is described as forward of distributor)
- [ ] Fuse link letter codes (E, N, Z etc.) and their locations — partially visible but unclear from OCR

---

## Related Pages

- [Electrical](../systems/electrical.md)
- [Engine](../systems/engine.md)
- [Fuel System](../systems/fuel-system.md)
