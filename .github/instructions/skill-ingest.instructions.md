# Skill: ingest

When the user asks to **ingest** one or more source files, follow this procedure exactly.

## Trigger phrases
"ingest", "ingest sources", "ingest raw/", "process this file", "add this source"

## Procedure

### 1. Identify the source file(s)
- If the user specifies a file or directory, use that.
- If not, default to all files in `raw/manuals/` that do not yet have a corresponding page in `wiki/sources/`.
- Never modify, rename, or delete files in `raw/`.

### 2. Read and extract
- Read the source file thoroughly.
- Extract facts relevant to the 1987 F-250 5.0L EFI V8 specifically (not generic multi-vehicle data).
- Note the exact file name — it will be the canonical citation throughout the wiki.

### 3. Create or update `wiki/sources/<slug>.md`
- Use a short, descriptive slug (e.g. `engine-shop-manual-1987`).
- Page must include:
  - Full title and file name
  - Origin / publication info
  - Contents summary (table of sections)
  - Key facts extracted (tables where possible)
  - Unresolved questions left by this source
  - Links to related wiki pages

### 4. Update related `wiki/systems/`, `wiki/maintenance/`, `wiki/problems/`, or `wiki/parts/` pages
- Add sourced facts; cite the filename in the Source column.
- Replace `_pending_` placeholders where data was found.
- If a claim conflicts with an existing sourced claim, note the conflict explicitly — do not silently overwrite.
- Mark uncertain facts as _uncertain_ rather than asserting them.
- Never invent or extrapolate facts not present in the source.

### 5. Update `wiki/index.md`
- Add the new source to the Sources table if it is not already listed.

### 6. Log the changes
- Append an entry to `wiki/log.md` with:
  - Date
  - Source file ingested
  - List of pages created or updated
  - Any caveats (OCR issues, uncertain data, conflicts)

## Quality rules
- Every claim in `wiki/` must cite a source filename.
- OEM manual data > forum/anecdotal data.
- If the source is an OCR scan, note OCR quality and flag uncertain table values.
- Do not fill in gaps with generic automotive knowledge — leave as `_pending_` with a question in Unresolved Questions.
