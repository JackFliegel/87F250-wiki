# Skill: lint

When the user asks to **lint** or **review** the wiki, follow this procedure exactly.

## Trigger phrases
"lint the wiki", "review the wiki", "check the wiki", "audit the wiki", "find problems"

## Procedure

### 1. Scan for unsupported claims
- Read each page in `wiki/systems/`, `wiki/maintenance/`, `wiki/problems/`, `wiki/parts/`.
- Flag any claim that lacks a Source citation.
- Flag any claim that says `_pending_` where related sources have since been ingested.

### 2. Check for contradictions
- Look for the same fact stated differently across pages.
- Look for facts in `wiki/` that conflict with content in `raw/` source files.
- If a conflict is found, note both versions and their sources — do not silently resolve.

### 3. Check for orphan pages
- Every page in `wiki/systems/`, `wiki/maintenance/`, `wiki/problems/`, `wiki/parts/` should be reachable from `wiki/index.md`.
- Every source page in `wiki/sources/` should be linked from at least one system/maintenance page.
- Flag any page not linked from anywhere.

### 4. Check for stale `_pending_` fields
- Compare `_pending_` fields against the ingested sources listed in `wiki/sources/`.
- If a source was ingested that answers a pending question, flag it as stale — the field should have been filled in.

### 5. Check source pages
- Every `wiki/sources/` page should correspond to a file in `raw/`.
- If a source page references a file that doesn't exist in `raw/`, flag it.

### 6. Report findings
- Present findings as a structured list grouped by category:
  - **Unsupported claims** (page → specific claim)
  - **Contradictions** (page A claim vs. page B claim, both with sources)
  - **Orphan pages**
  - **Stale pending fields** (page → field → which source has the answer)
  - **Broken source references**
- Be conservative — only flag genuine issues, not style differences.
- Do **not** silently rewrite content. Show the proposed change and ask before making it, unless the fix is trivial (e.g. a broken relative link).

## What lint does NOT do
- Does not invent or add facts.
- Does not rewrite prose style.
- Does not delete pages.
- Does not modify files in `raw/`.
