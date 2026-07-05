# EEC-IV Self-Test Procedure (Quick Test)

**Summary:** Step-by-step procedure to run the EEC-IV Key On Engine Off (KOEO) and Engine Running (KOER) self-tests on the 1987 F-250 5.0L EFI.

**Applicability:** 1987 Ford F-250, 5.0L EFI V8, EEC-IV system

**Sources:**
- `Full text of Engine Emissions Diagnosis.md` — Section 16: EEC IV Quick Test, All Engines

---

## What You Need

- **Analog voltmeter (VOM)** — 0–15V DC scale (cheapest option), OR
- **STAR Tester** — Rotunda 007-00017 or equivalent (displays codes as numbers)
- **Jumper wire** — to bridge Self-Test Input (STI) to Signal Return
- **Timing light** (for computed timing check — optional for code-pulling only)

## Connector Location

The Self-Test connector and Self-Test Input (STI) connector are located **in the engine compartment, near each other**. On the 5.0L EFI truck, they are typically found near the ECA (computer) harness routing — look near the driver-side fender apron or firewall area.

The large Self-Test connector has multiple pins:
- **Pin 2** — Signal Return (SIG RTN)
- **Pin 4** — Self-Test Output (STO)
- The **STI connector** is a separate small single-pin connector nearby

> _Note: Exact physical location not confirmed from OCR; typically near the firewall on the driver side._  
> Source: `Full text of Engine Emissions Diagnosis.md`, Section 16 & `Full text of Electrical Vacuum Troubleshooting.md`

---

## Step 1.0 — Visual Check & Vehicle Preparation

Before running codes, perform these checks:

1. Inspect air cleaner and inlet ducting
2. Check **all engine vacuum hoses** for damage, leaks, cracks, blockage, proper routing
3. Check EEC-IV wiring harness for proper connections, bent/broken pins, corrosion, loose wires
4. Check processor, sensors, and actuators for physical damage
5. Check engine coolant level
6. Make any necessary repairs before proceeding

**Vehicle Preparation:**
1. Apply parking brake; shift to Park (or Neutral for manual trans)
2. Block drive wheels
3. Turn off ALL electrical loads (radio, lights, A/C blower, etc.)
4. Start engine and run until at **operating temperature** (upper radiator hose hot and pressurized)
5. Turn engine off — proceed to Step 2.0

---

## Step 2.0 — Equipment Hookup

### Using an Analog Voltmeter (VOM):

1. Turn ignition key OFF
2. **DO NOT** connect the jumper wire yet (that activates the test)
3. Set VOM to DC voltage, 0–15V range
4. Connect VOM **positive (+)** lead to the **Self-Test Output pin (STO, Pin 4)** on the large Self-Test connector
5. Connect VOM **negative (−)** lead to **battery negative terminal**
6. Connect timing light if checking timing

### Using a STAR Tester:

1. Turn ignition key OFF
2. Connect the color-coded adapter cable to the STAR tester
3. Connect adapter cable leads to the Self-Test connectors
4. Connect timing light if checking timing

---

## Step 3.0 — Key On Engine Off (KOEO) Self-Test

> **Important for 5.0L Truck:** The steering wheel must be turned **one-half turn and released** after the ID code is displayed during the Engine Running test (Step 5.0). This is NOT required during KOEO.

### How to Run:

1. Verify vehicle prepared per Steps 1.0 and 2.0
2. Place ignition key in the **ON (RUN)** position — **do NOT start the engine**
3. **Activate Self-Test:**
   - STAR Tester: Latch the center button in the down position
   - Analog VOM: Connect jumper wire from **STI connector** to **Signal Return (Pin 2)** on the Self-Test connector
4. **Record all service codes displayed**
5. Proceed to interpret codes (see Code Output section below)

### DON'T:
- Do NOT depress the throttle during KOEO Self-Test

### Code Output Format (KOEO):

```
[Key On Engine Off codes] — [Separator pulse] — [Continuous Memory codes]
```

- **Code 11** = PASS (system OK)
- **11 — separator — 11** = Both KOEO and Continuous Memory pass
- Any other code = fault detected (see Service Code Table below)

---

## Step 4.0 — Computed Timing Check (Optional)

1. Turn key OFF, wait 10 seconds
2. Start engine
3. Activate Self-Test per Step 3.0 procedure
4. After the last service code is displayed, check timing with timing light
5. **Self-Test timing = Base timing + 20° BTDC ± 3°** (check VECI decal for base timing)

Example: If base timing is 10° BTDC → Self-Test timing should be 27°–33° BTDC.

---

## Step 5.0 — Engine Running (KOER) Self-Test

### How to Run:

1. **Deactivate** Self-Test (remove jumper / unlatch STAR)
2. Start engine and run at **2,000 RPM for 2 minutes** (this warms up the EGO/HEGO sensor)
3. Turn engine OFF, wait **10 seconds**
4. **Start engine** again
5. **Activate Self-Test** (jumper STI to SIG RTN, or latch STAR)
6. After the **ID code** is displayed, **turn the steering wheel one-half turn and release** (required for 5.0L truck)
7. If a **Dynamic Response Code** is displayed (single pulse), perform a brief **wide-open throttle (WOT) snap** and release
8. **Record all service codes displayed**

### DON'T:
- Do NOT depress the throttle unless a Dynamic Response Code is displayed

### Code Output Format (Engine Running):

```
[ID Code] — [Dynamic Response (or none)] — [Engine Running codes]
```

- ID code = 2(0), 3(0), or 4(0) identifies the processor
- **Code 11** after the ID = PASS
- **Code 98** in place of ID = vehicle did not pass KOEO test first; go back and fix KOEO codes

---

## Reading Codes on an Analog Voltmeter

The codes appear as **needle sweeps (pulses)** on the VOM:

- Each pulse = one count for that digit
- **2-second pause** separates the two digits of a code
- **4-second pause** separates one code from the next
- **6-second delay + single half-second sweep + 6-second delay** = separator between KOEO codes and Continuous Memory codes

**Example:** Code 23 appears as:
- 2 needle sweeps → 2-second pause → 3 needle sweeps → 4-second pause → next code

---

## Light Truck Service Codes (5.0L EFI)

### KOEO Codes:

| Code | Meaning |
|------|---------|
| 11 | PASS — system OK |
| 15 | Power/ECA issue (Pinpoint Test Q10) |
| 21 | ECT (Engine Coolant Temp) out of range |
| 22 | MAP/BP sensor out of range |
| 23 | TPS (Throttle Position Sensor) out of range |
| 24 | ACT (Air Charge Temp) out of range |
| 31 | EVP (EGR Valve Position) out of range |
| 32 | EGR Valve not seated |
| 34 | EVP voltage above closed limit |
| 35 | EVP voltage below closed limit |
| 51 | ECT signal out of Self-Test range |
| 52 | PSPS (Power Steering Pressure Switch) |
| 53 | TPS signal out of Self-Test range |
| 54 | ACT signal out of Self-Test range |
| 61 | ECT signal grounded |
| 63 | TPS signal grounded |
| 64 | ACT signal grounded |
| 67 | Neutral/Drive switch open (A/T) or clutch switch (M/T) |
| 81 | Air management — TAB circuit failure |
| 82 | Air management — TAD circuit failure |
| 83 | EGR control — low solenoid |
| 84 | EGR control — EVR circuit failure |
| 85 | Canister purge solenoid failure |
| 87 | Fuel pump circuit failure |
| 89 | Torque converter clutch or EGR cutoff circuit |

### Engine Running Codes:

| Code | Meaning |
|------|---------|
| 11 | PASS — system OK |
| 12 | RPM unable to reach upper test limit |
| 13 | RPM unable to reach lower test limit |
| 16 | RPM too low to perform fuel test |
| 21 | ECT out of range |
| 22 | MAP/BP out of range |
| 23 | TPS out of range |
| 24 | ACT out of range |
| 25 | Knock sensor not detected |
| 31 | EVP out of range |
| 32 | EGR valve not seated |
| 33 | EGR valve not opening |
| 34 | EVP voltage above closed limit |
| 35 | EVP voltage below closed limit |
| 38 | Idle track switch open at idle |
| 41 | HEGO (O2 sensor) lean — system always lean |
| 42 | HEGO rich — system always rich |
| 44 | Air management — TAB or TAD flow fault |
| 45 | Air management — upstream flow not detected |
| 46 | Air management — not bypassed |
| 52 | PSPS circuit open |
| 72 | Insufficient MAP change during dynamic response |
| 73 | Insufficient TPS change during dynamic response |
| 74 | Brake On/Off (BOO) switch failure |
| 75 | Brake On/Off (BOO) switch — no toggling detected |
| 77 | Brief WOT not detected during dynamic response |
| 98 | KOEO Self-Test not passed — fix KOEO codes first |

### Continuous Memory Codes:

Continuous Memory captures **intermittent** faults that occurred in the last 40 warm-up cycles. These are output after the separator during the KOEO test.

---

## Clearing Continuous Memory Codes

1. Run Key On Engine Off Self-Test per Step 3.0
2. When Service Codes **begin to be displayed**, immediately deactivate Self-Test:
   - STAR: Unlatch the center button (up position)
   - VOM: Remove the jumper wire
3. Codes are now cleared

> Codes will also automatically erase after 41 engine warm-up cycles without recurrence.

---

## After the Test

- **Code 11 everywhere** = EEC-IV system is OK; problem is likely non-EEC (mechanical — fuel filter, ignition components, vacuum leaks, IAC sticking)
- **Any fault code** = follow the Pinpoint Test for that code in the Engine Emissions Diagnosis Manual
- After any repair, re-run Steps 3.0, 5.0, and 6.0 to verify the fix

---

## Related Pages

- [Electrical / EEC-IV system](../systems/electrical.md)
- [Fuel system](../systems/fuel-system.md)
- [Active issues — Hard Start](../truck/active-issues.md)
- [Common issues](../problems/common-issues.md)
- [Engine Emissions Diagnosis source](../sources/engine-emissions-diagnosis-1987.md)
