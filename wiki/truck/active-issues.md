---
type: Issue Log
title: Active Issues
description: Open and monitoring issues specific to this truck.
tags: [this-truck, issues, active]
timestamp: 2026-07-01T00:00:00Z
---

# Active Issues

**Summary:** Open and monitoring issues specific to this truck.

**Applicability:** This truck only.

**Sources:** Populated from `raw/personal/` notes via the `track` skill.

---

<!-- Add issues below using the format defined in skill-track.instructions.md -->

## Hard Start / No Start with Choppy Idle

| Field | Value |
|---|---|
| Status | active |
| First noticed | 2026-04-19 |
| Last updated | 2026-07-01 |
| Confidence | low |

**Summary:** Truck cranks and occasionally sputters to life but will not sustain idle and dies.

**Symptoms:**
- Engine cranks but does not start cleanly
- Occasional brief start with very rough, choppy idle
- Engine stalls shortly after brief starts

**Conditions:**
- Observed during normal start attempt
- Battery confirmed charged; terminals confirmed secure

**Suspected systems:**
- Fuel delivery (low fuel pressure, failing pump, clogged filter)
- Ignition (TFI module, distributor cap/rotor, spark plug wires)
- EEC-IV / sensors (TPS, MAP, ACT, ECT — bad reading preventing stable idle)
- IAC (idle air control) — if engine starts and immediately idles rough, IAC or vacuum leak possible

**Evidence:**
- 2026-04-19: Engine turns over, sputters, briefly starts with choppy idle, then dies
- 2026-04-19: Battery charged and terminals tight — electrical supply is not the issue
- 2026-07-01: Truck cranked and started fine. Ran rough initially but smoothed out as engine warmed up. No modifications made since April. Ambient temperature noticeably warmer than April 19 attempt. Truck able to sustain idle and run — significant improvement over April behavior.

**Diagnostics performed:**
- _None yet_

**Repairs or changes made:**
- _None yet_

**Current assessment:**
The truck now starts and runs, which is a major improvement over April when it would not sustain idle. The key new variable is temperature — both warmer ambient air and the improvement as the engine warms up. This pattern strongly suggests a temperature-sensitive component or condition:

1. **ECT sensor** — if reading incorrectly when cold, the EEC-IV will command a wrong air/fuel mixture at startup. As the engine warms and the sensor begins reading more accurately (or moves into a range where its error matters less), the mixture corrects.
2. **IAC valve** — carbon buildup or sticking can cause rough cold idle that clears as the valve warms and loosens.
3. **Marginal fuel pressure** — a weak pump or partially clogged filter may deliver _enough_ fuel once engine is warm and fuel demand stabilizes, but struggle during cold enrichment.
4. **Ignition components (cap/rotor/wires)** — old or cracked components can arc or misfire in cold/damp conditions and improve as under-hood temps rise.

The fact that no modifications were made and the truck now runs suggests temperature/season was the primary variable — the underlying issue may still be present but less severe in warm weather. Cause remains _suspected_, not confirmed.

**Recommended next steps to ensure reliable running:**
1. **Run EEC-IV KOEO and KOER self-tests** — check for stored fault codes; this is free and fast.
2. **Measure fuel pressure** at the Schrader valve (spec: 35–45 psi running). Low pressure confirms pump/filter issues.
3. **Inspect and replace fuel filter** — the truck has been sitting and the filter may be partially occluded. Cheap insurance.
4. **Inspect distributor cap, rotor, spark plug wires** for cracks, corrosion, carbon tracking.
5. **Inspect/clean IAC valve** — remove and clean with throttle body cleaner.
6. **Check/replace spark plugs** — verify gap (check VECI decal on truck; likely 0.044–0.054").
7. **Fresh fuel** — if any of the fuel in the tank is from April or earlier, consider adding fresh fuel or a stabilizer.
8. **Check all vacuum hoses** — brittle/cracked hoses cause lean conditions especially at idle.

**Related pages:**
- [Fuel system](../systems/fuel-system.md)
- [Electrical / EEC-IV](../systems/electrical.md)
- [Common issues](../problems/common-issues.md)

**Source notes:**
- No raw/personal source yet — based on owner-reported symptoms

---

## Related pages

- [My truck](my-truck.md)
- [Resolved issues](resolved-issues.md)
- [Common issues (general)](../problems/common-issues.md)
