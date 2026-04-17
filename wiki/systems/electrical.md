# Electrical System

**Summary:** Wiring, fuses, sensors, and ignition system notes for the 1987 F-250 5.0 EFI V8.

**Applicability:** 1987 Ford F-250, 5.0 EFI V8  
**Sources:**
- `Full text of Electrical Vacuum Troubleshooting.md` (EVTM — Sections 15/19, 39/40, 54)
- `Full text of Engine Shop Manual.md` (Section 23-01 — Ignition; Section 24-35 — Fuel Pump)
- `Full text of Engine Emissions Diagnosis.md` (EEC-IV system descriptions)

---

## Fuse Panel (Gasoline)

The fuse panel is dash-mounted. Fuse positions and protected circuits per the EVTM:

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

**Always-hot fuses:** Positions 1, 4, 8, 12, and others — powered regardless of ignition switch position.

**Fuse color codes:** 4A=Pink, 5A=Tan, 10A=Red, 15A=Light Blue, 20A=Yellow, 25A=Natural, 30A=Light Green

Source: EVTM, page 19

---

## Power Distribution

- Alternator and Battery connected at Starter Relay hot terminal
- High-current circuits protected by **fuse links** (not fuse panel) — fuse links E, N, Z and others
- Low-current circuits protected by fuse panel fuses
- Fuse link locations: partially described in EVTM; near starter relay

Source: EVTM, pages 18–19

---

## Ignition System

| Item | Detail | Source |
|------|--------|--------|
| System | TFI-IV (Thick Film Integration IV) | Engine Shop Manual §23-01 |
| Engine management | EEC-IV | Engine Shop Manual §23-01 |
| Distributor type | Universal distributor; Hall effect vane switch | Engine Shop Manual §23-01 |
| Distributor trigger | PIP (Profile Ignition Pickup) sensor | Engine Shop Manual §23-01 |
| TFI module function | Controls dwell; limits primary current; passes SPOUT to EEC-IV | Engine Shop Manual §23-01 |
| Spark plugs | 14mm, ½" standard reach, tapered seat | Engine Shop Manual §23-01 |
| Spark plug (part) | ASF-52G _(uncertain — from sample 1985 decal; verify 1987 engine decal)_ | Engine Emissions Diagnosis §1 |
| Spark plug gap | 0.048–0.052" _(uncertain — same caveat)_ | Engine Emissions Diagnosis §1 |
| Timing | Controlled by EEC-IV; **not a normal field adjustment** on TFI-IV | Engine Shop Manual §23-01 |
| Base timing (open-loop) | If SPOUT signal wire is open, TFI defaults to PIP-based timing | Engine Shop Manual §23-01 |
| Octane adjustment | Permitted per EEC-IV system; see emissions decal | Engine Shop Manual §23-01 |

---

## EEC-IV System

The Electronic Engine Control-IV (EEC-IV) system manages:
- Air/fuel ratio (injector pulse width)
- Ignition timing (via SPOUT signal to TFI module)
- EGR flow (EGR Vacuum Regulator solenoid)
- Thermactor air flow (TAB and TAD solenoids)
- Idle speed (Throttle Air Bypass Valve solenoid)

Source: EVTM §40/54; Engine Emissions Diagnosis Part II

### ECA (Electronic Control Assembly) Location

**Behind the LH (driver-side) kick panel.** Source: EVTM §54 component location table

### Self-Test (KOEO / KOER)

- **KOEO** = Key On Engine Off test
- **KOER** = Key On Engine Running test
- VIP Self-Test Connector: Shown in EEC wiring diagram; physical location _uncertain from OCR_ — typically near ECA or in engine compartment
- Diagnostic codes output as numeric pulses; full code list in Engine Emissions Diagnosis Manual §16

---

## EEC-IV Sensor Locations (5.0L EFI — 50 States)

| Sensor / Component | Location | Source |
|--------------------|----------|--------|
| Air Charge Temperature (ACT) Sensor | #6 lower intake manifold runner | EVTM §54 |
| Engine Coolant Temperature (ECT) Sensor | At intake manifold heater hose elbow | EVTM §54 |
| Throttle Position Sensor (TPS) | Connected to throttle body shaft | EVTM §54 |
| Manifold Absolute Pressure (MAP) Sensor | On bracket on intake manifold | EVTM §54 |
| Knock Sensor (KS) | In cylinder block, behind the intake manifold | EVTM §54 |
| EGR Vacuum Regulator (EVR) Solenoid | On bracket on intake manifold | EVTM §54 |
| EGR Valve Position (EVP) Sensor | At EGR valve on intake manifold | EVTM §54 |
| Thermactor Air Bypass (TAB) Solenoid | On bracket on intake manifold | EVTM §54 |
| Thermactor Air Diverter (TAD) Solenoid | On bracket on intake manifold | EVTM §54 |
| Throttle Air Bypass Valve Solenoid | On throttle body | EVTM §54 |
| Heated Exhaust Gas Oxygen (HEGO) Sensor | In communicator tube connecting both exhaust pipes | EVTM §54 |
| Power Steering Pressure Switch | In power steering pressure hose near steering gear | EVTM §54 |
| Vehicle Speed Sensor (VSS) | At transmission | EVTM §54 |
| EEC Power Relay | Under plastic shield at air cleaner support bracket | EVTM §54 |
| Fuel Pump Relay | Under plastic shield at air cleaner support bracket | EVTM §54 |
| ECA (EEC Module) | Behind LH kick panel | EVTM §54 |
| EEC Clutch Switch | Above clutch pedal | EVTM §54 |

**Note on MAP vs. MAF:** Engine Shop Manual §24-05 describes the 5.0L EFI as "mass air flow" type, but the sensor list and EVTM confirm a MAP (Manifold Absolute Pressure) sensor — consistent with a speed-density fuel calculation. No mass airflow meter is listed. This may be imprecise language in the shop manual or an OCR artifact.

---

## Grounds

- Engine grounds G801 and G802: Apply to both 4.9L and 5.0L gasoline engines
- Ground locations: EVTM page 5; specific locations partially obscured by OCR

Source: EVTM

---

## Known Notes

- **Timing is EEC-IV controlled:** Do not adjust base timing by swapping octane rods without proper authorization; federal emissions requirements will be affected. Source: Engine Shop Manual §23-01
- **TFI module failure mode:** If SPOUT wire opens, engine defaults to base timing only — this can present as severe retarded timing / poor performance. Source: Engine Shop Manual §23-01

---

## Unresolved Questions

- [ ] Confirm alternator output spec (amperage rating)
- [ ] Confirm VIP Self-Test Connector physical location
- [ ] Complete EEC-IV fault code list — requires deeper extraction of Engine Emissions Diagnosis §16
- [ ] Fuse link locations and amperage ratings
- [ ] Confirm spark plug and gap for actual 1987 F-250 calibration number (read from engine decal)

---

## Related Pages

- [Engine](engine.md)
- [Fuel System](fuel-system.md)
- [Common Issues](../problems/common-issues.md)
- [Source: EVTM](../sources/electrical-vacuum-troubleshooting-1987.md)
- [Source: Engine Shop Manual](../sources/engine-shop-manual-1987.md)
- [Source: Engine Emissions Diagnosis](../sources/engine-emissions-diagnosis-1987.md)
