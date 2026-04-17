## Purpose

This repository is a persistent knowledge base for a 1987 Ford F-250.

## Architecture

- `raw/` contains immutable source material.
- `wiki/` contains synthesized markdown pages.
- Never edit, rename, summarize in place, or delete files in `raw/`.
- Treat `raw/archive/` as cold storage for original large files.
- Prefer `raw/manuals/`, `raw/images/`, and `raw/personal/` as active source material.

## Source handling

- Every substantial claim in `wiki/` should reference one or more source files by filename.
- If information conflicts across sources, note the conflict explicitly.
- If a claim seems uncertain, mark it as uncertain instead of asserting it as fact.
- Prefer OEM/manual information over forum-style or anecdotal information.
- Prefer specific source-backed notes over generic automotive knowledge.

## Wiki structure

Create or update pages in:

- `wiki/sources/` for source summaries
- `wiki/systems/` for truck systems (engine, wiring, fuel, brakes, etc.)
- `wiki/problems/` for symptoms and troubleshooting
- `wiki/maintenance/` for procedures
- `wiki/parts/` for part numbers and compatibility
- `wiki/synthesis/` for higher-level cross-source summaries

## Page conventions

- Use markdown only
- Start each page with:
    - Title
    - Short summary
    - Known applicability (engine, trim, transmission, emissions if known)
    - Source list
- Link related pages with relative markdown links
- Update `wiki/index.md` when adding important new pages
- Append major changes to `wiki/log.md`

## Ingest behavior

When asked to ingest a source:

1. Do not modify the raw file
2. Create or update a corresponding page in `wiki/sources/`
3. Update related system/problem/maintenance pages
4. Add unresolved questions if the source leaves ambiguity
5. Log the changes in `wiki/log.md`

## Review behavior

When asked to review the wiki:

- Look for contradictions
- Look for stale or unsupported claims
- Look for orphan pages and missing cross-links
- Suggest changes conservatively
- Do not silently rewrite large amounts of content without showing the edits

## Truck-specific issues

Truck-specific observations belong in `wiki/truck/`, not in general system/problem pages. See the `track` skill below and `.github/instructions/skill-track.instructions.md` for the full procedure.

## Skills

Named procedures are defined in full detail in `.github/instructions/`. The summaries below are quick references.

### `ingest`

**Trigger:** "ingest", "ingest sources", "process this file"  
**What it does:** Reads one or more files from `raw/`, extracts facts relevant to the 1987 F-250 5.0L EFI, creates/updates `wiki/sources/<slug>.md`, updates related system/maintenance pages with cited facts, updates `wiki/index.md`, and logs changes in `wiki/log.md`.  
**Full procedure:** `.github/instructions/skill-ingest.instructions.md`

### `lint`

**Trigger:** "lint the wiki", "review the wiki", "audit the wiki"  
**What it does:** Scans `wiki/` for unsupported claims, contradictions between pages or against sources, orphan pages, stale `_pending_` fields that sources have since answered, and broken source references. Reports findings grouped by category. Does not silently rewrite — shows proposed changes before applying.  
**Full procedure:** `.github/instructions/skill-lint.instructions.md`

### `track`

**Trigger:** "track issue", "log issue", "add issue", "update my truck", "mark resolved", "new problem", "my truck has"  
**What it does:** Creates or updates truck-specific issue entries in `wiki/truck/active-issues.md`, using a structured format with status, symptoms, evidence, diagnostics, and repairs. Keeps observations about this truck separate from general model knowledge. Moves confirmed fixes to `wiki/truck/resolved-issues.md`. Updates `wiki/log.md`.  
**Full procedure:** `.github/instructions/skill-track.instructions.md`
