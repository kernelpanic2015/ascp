# ASCP Schema — Version 0.1

This document defines the minimum structured formats for the project manifest and for individual jobs.

Formal JSON Schemas are also provided under `schema/`.

## 1. Project Manifest (`ascp/manifest.json`)

Minimal required structure:

```json
{
  "ascp_version": "0.1.0",
  "project": {
    "name": "string",
    "description": "string",
    "repository": "https://github.com/owner/repo",
    "license": "MIT",
    "category": "protocol | library | application | documentation | tooling | other",
    "homepage": "optional url",
    "contact": "optional"
  },
  "jobs": [
    {
      "id": "001",
      "path": "ascp/jobs/job-001.json"
    }
  ],
  "registry": {
    "listed": true,
    "notes": "optional"
  }
}
```

### Field notes

- `ascp_version`: protocol version this manifest follows.
- `project.category`: used for filtering in the registry.
- `jobs`: list of job references (id + path to the job file).
- Jobs can also be inlined in a future version; for 0.1 we prefer separate files.

## 2. Job (`ascp/jobs/job-XXX.json`)

Minimal required structure:

```json
{
  "id": "001",
  "title": "Short clear title",
  "status": "open",
  "priority": "P1",
  "category": "documentation | code | design | research | other",
  "difficulty": "beginner | intermediate | advanced",
  "description": "Clear description of what needs to be done.",
  "acceptance_criteria": [
    "Criterion 1",
    "Criterion 2"
  ],
  "suggested_files": [
    "path/to/file.md"
  ],
  "labels": ["docs", "good-first-job"],
  "estimated_effort": "small | medium | large",
  "created_at": "2026-09-06",
  "updated_at": "2026-09-06"
}
```

### Status values (v0.1)

- `open` — available to be claimed
- `claimed` — someone is working on it (optional tracking)
- `done` — completed / PR merged or accepted
- `cancelled`

### Priority

- `P0` — critical
- `P1` — high
- `P2` — normal
- `P3` — low / nice-to-have

## 3. Design principles for v0.1

- Keep it simple and readable by both humans and agents.
- Prefer explicit fields over clever conventions.
- Allow future extension without breaking existing manifests.
- Make it easy for a maintainer to create the first job manually.

## 4. Validation

In later versions a validation skill/prompt will check:

- Required fields presence
- License compatibility
- Job quality signals
- Basic repository health

For now, human review + the rules in ENTRY_RULES.md are the gate.
