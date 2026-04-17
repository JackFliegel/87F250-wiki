# Wiki Change Log

---

## 2026-04-17 — Ingested three OEM manuals from raw/manuals/

**Sources ingested:**

| File | Manual | Pages |
|------|--------|-------|
| `Full text of Engine Shop Manual.md` | 1987 Ford Light Truck Engine Shop Manual B | 574 |
| `Full text of Electrical Vacuum Troubleshooting.md` | 1987 Bronco/F150–F350 EVTM | 151 |
| `Full text of Engine Emissions Diagnosis.md` | 1987 Engine & Emissions Diagnosis Manual H | 1,147 |

**New source pages created:**
- `wiki/sources/engine-shop-manual-1987.md`
- `wiki/sources/electrical-vacuum-troubleshooting-1987.md`
- `wiki/sources/engine-emissions-diagnosis-1987.md`

**System pages updated with sourced facts:**

- `wiki/systems/engine.md` — Added: bore×stroke (4.00"×3.00"), firing order (1-5-4-2-6-3-7-8), oil pressure (40–60 psi), oil capacity (6 qt w/filter), block/crank/piston materials, rocker arm lift ratio (1.61:1), combustion chamber volume (60.6–63.6 cc), ignition system type (TFI-IV/EEC-IV), aluminum intake manifold note, spark plug size (14mm tapered seat), VIN position 8 code (likely N, uncertain), unleaded fuel requirement
- `wiki/systems/electrical.md` — Added: full 18-position fuse panel table with amperage and circuit coverage, power distribution description, fuse color codes, complete EEC-IV sensor location table for 5.0L (ACT, ECT, TPS, MAP, KS, EVR, EVP, TAB, TAD, TABV, HEGO, PSPS, VSS), ECA location (LH kick panel), EEC power relay and fuel pump relay location, TFI-IV ignition detail, KOEO/KOER self-test description, MAP vs. MAF discrepancy noted
- `wiki/systems/fuel-system.md` — Added: two-pump system description (in-tank low pressure + chassis high pressure), fuel pressure specs (35–45 psi running; 35–45 psi hold 60 sec after key-off), high pressure pump specs (39 psi / 60 L/hr), inertia switch location (toe-board right of trans hump), fuel pump control by EEC-IV (120 rpm shutoff), key-on pre-pressurization detail, injector part number (9F593), pressure regulator part number (9C968), injector firing sequence (two banks of 4)
- `wiki/maintenance/fluids-and-service.md` — Added: oil capacity (6 qt / 5.6 L with filter; 5 qt / 4.7 L without), thermostat open range (180–192°F start, 200–212°F fully open), spark plug size note, VECI decal guidance for plug spec

**Index updated:** Sources section added to `wiki/index.md`

**Caveats recorded:**
- OCR quality is variable throughout all three manuals; table alignment may be off
- Spark plug part number (ASF-52G) and gap (0.048–0.052") are from a sample 1985 calibration decal — must verify against actual 1987 F-250 engine decal
- VIN position 8 engine code for 5.0L EFI is likely N but OCR table alignment is uncertain
- Thermostat spec was found in diesel engine section — needs cross-check against gasoline cooling system section
- Compression ratio, horsepower, torque, coolant capacity not yet extracted
- EEC-IV fault code list not extracted from Emissions Diagnosis §16

---

## 2026-04-17 — Initial scaffold

**Action:** Created starter wiki pages for the 1987 Ford F-250 EFI 5.0 V8 knowledge base.

**Pages created:**
- `wiki/index.md` — top-level index with links to all sections
- `wiki/systems/engine.md` — engine specs and component placeholders
- `wiki/systems/electrical.md` — wiring, fuses, sensors, EEC-IV notes
- `wiki/systems/fuel-system.md` — fuel delivery, pressure, injector placeholders
- `wiki/problems/common-issues.md` — symptom/issue index with template
- `wiki/maintenance/fluids-and-service.md` — fluid specs and service interval table
- `wiki/parts/known-part-categories.md` — part number index by system

**Notes:**
- No raw sources ingested yet; all spec fields were marked `_pending_`
- All pages include cross-links to related pages
- Unresolved questions captured per page for follow-up after source ingestion
- No facts invented; placeholders used throughout

