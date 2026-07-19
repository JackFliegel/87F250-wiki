# Bundle Update Log

## 2026-07-05

* **Migration**: Converted the bundle to Open Knowledge Format (OKF) v0.1. Added YAML frontmatter (`type`, `title`, `description`, `tags`, `timestamp`) to every concept document under `systems/`, `problems/`, `maintenance/`, `parts/`, `sources/`, and `truck/`.
* **Update**: Reformatted [index](index.md) into OKF §6 progressive-disclosure sections and declared `okf_version: "0.1"` in its frontmatter.
* **Update**: Reformatted this log into OKF §7 date-grouped form (ISO 8601 headings, newest first).
* **Creation**: Added per-directory `index.md` listings for each subdirectory.

## 2026-07-01

* **Update**: Revised active issue "Hard Start / No Start with Choppy Idle" in [active issues](truck/active-issues.md) with 2026-07-01 evidence, updated assessment, and next steps. Owner reports the truck started and ran with no modifications, running rough then smoothing as it warmed — suggesting a temperature correlation. Suspects narrowed to ECT sensor, IAC valve, marginal fuel pressure, ignition components, and stale fuel.
* **Creation**: Added [EEC-IV Self-Test](maintenance/eec-iv-self-test.md) — full KOEO/KOER Quick Test procedure with equipment hookup, analog-voltmeter code reading, and Light Truck Service Code charts for the 5.0L EFI, extracted from Engine Emissions Diagnosis Manual §16.
* **Update**: Added the self-test page to the [index](index.md).

## 2026-04-19

* **Creation**: Added active issue "Hard Start / No Start with Choppy Idle" to [active issues](truck/active-issues.md). Owner reports the truck cranks, occasionally sputters to life with a rough choppy idle, then dies; battery and terminals ruled out; no diagnostics performed yet. Suspected (unconfirmed) causes: fuel delivery, ignition, EEC-IV sensor fault, or IAC/vacuum leak. Next steps: measure fuel pressure at the Schrader valve and run the EEC-IV KOEO self-test.

## 2026-04-17

* **Update**: Added fuel filter installation detail from Engine Shop Manual §24-51 to [fuel system](systems/fuel-system.md) and [fluids & service](maintenance/fluids-and-service.md). Filter is on the frame rail between the high-pressure pump and engine; a flow arrow on the body must point toward the engine; clamp torque 1.7–2.8 N·m (15–25 in-lb). Manual states the filter "should last the life of the vehicle under normal driving conditions." Exact part numbers remain unconfirmed for the 5.0L EFI (Fig. 3 labels base assembly 9B072, tube assembly 9J338).
* **Ingestion**: Ingested three OEM manuals and created source summary pages.

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

* **Initialization**: Created the starter bundle for the 1987 Ford F-250 EFI 5.0 V8. Established [index](index.md), [engine](systems/engine.md), [electrical](systems/electrical.md), [fuel system](systems/fuel-system.md), [common issues](problems/common-issues.md), [fluids & service](maintenance/fluids-and-service.md), and [known part categories](parts/known-part-categories.md). No raw sources ingested yet — all spec fields marked `_pending_`; cross-links added between pages; no facts invented.

