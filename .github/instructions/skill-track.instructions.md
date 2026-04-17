# Skill: track

When the user asks to **track**, **log**, **update**, or **resolve** an issue specific to their truck, follow this procedure exactly.

## Trigger phrases
"track issue", "log issue", "add issue", "update my truck", "mark resolved", "new problem", "my truck has", "update issue", "close issue"

## Core principle
This skill keeps observations about **this specific truck** separate from general 1987 F-250 knowledge.
- Do NOT treat observations from this truck as universal facts about all 1987 F-250s.
- When a truck-specific issue resembles a known common issue, **link** to the general problem page rather than merging the two.
- Preserve uncertainty. Distinguish clearly between:
  - observed symptoms
  - suspected causes
  - confirmed causes
  - completed repairs
  - unresolved questions

## Storage model
| Content type | Location |
|---|---|
| Raw personal notes, photos, receipts | `raw/personal/` (immutable) |
| Truck identity and build details | `wiki/truck/my-truck.md` |
| Active and monitoring issues | `wiki/truck/active-issues.md` |
| Resolved issues (archived) | `wiki/truck/resolved-issues.md` |
| General model knowledge | `wiki/systems/`, `wiki/problems/`, `wiki/maintenance/`, `wiki/parts/` |

## Procedure

### 1. Read context
- Check `wiki/truck/active-issues.md` and `wiki/truck/my-truck.md` for existing state.
- If the user references a raw personal file, read it from `raw/personal/`. Never modify it.

### 2. Create or update the issue entry

Each issue entry in `wiki/truck/active-issues.md` must use this format:

```markdown
## <Issue Title>

| Field | Value |
|---|---|
| Status | active / monitoring / resolved |
| First noticed | <date or "unknown"> |
| Last updated | <date> |
| Confidence | low / medium / high |

**Summary:** One-sentence description.

**Symptoms:**
- …

**Conditions:**
- When does it occur? Temp, speed, load, etc.

**Suspected systems:**
- …

**Evidence:**
- <dated observation or measurement>

**Diagnostics performed:**
- …

**Repairs or changes made:**
- …

**Current assessment:**
Narrative of where things stand and what is still unknown.

**Related pages:**
- [System page](../systems/…)
- [Problem page](../problems/…)

**Source notes:**
- raw/personal/<filename> — <brief description>
```

### 3. Handle status transitions
- **active → monitoring:** A repair was attempted but outcome is unclear. Do not mark resolved until evidence supports it.
- **monitoring → resolved:** Confirmed fix with follow-up evidence. Move the entry to `wiki/truck/resolved-issues.md`.
- **resolved → active:** If a previously resolved issue recurs, restore it to active with a note about recurrence.

### 4. Update `wiki/truck/my-truck.md`
If the user provides new information about the truck's identity, build, mileage, or modification history, update `wiki/truck/my-truck.md` accordingly. Cite the source.

### 5. Update `wiki/log.md`
Append an entry with:
- Date
- Issue title and status change
- Pages created or updated
- Any caveats

## Evidence policy
- Prefer direct observations, dated notes, photos, measurements, and repair actions over speculation.
- Do not overstate certainty.
- Mark unconfirmed causes as _suspected_ rather than _confirmed_.

## What this skill does NOT do
- Does not modify files in `raw/`.
- Does not add truck-specific observations to general `wiki/systems/` or `wiki/problems/` pages as facts.
- Does not invent symptoms or causes not supported by evidence.
- Does not silently move issues to resolved without user confirmation.
