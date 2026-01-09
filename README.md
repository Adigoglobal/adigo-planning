# adigo-planning

This repository is the single source of truth for ADIGO planning, canon, and PRD review. No application code here.

Contents
- docs/canon/*: Canonical frameworks (responsive web, copywriting)
- docs/instructions/*: Paste‑ready instructions for CodeSpring/Cursor (AdiGig Admin ↔ Mobile linking, Map UX, AI pane, P0 plan/DoD)
- docs/prd/adigig-admin/*: Frontend/Backend/Database PRD stubs (linking to CodeSpring canonical node IDs) + acceptance checklists, AI analyst, map UX
- docs/mindmap/latest/meta.json: Mindmap snapshot metadata (ID, canonical bridge, counts)

Workflow
- Propose changes via PRs to this repo before implementing in app repos
- Keep mindmap canonical IDs in frontmatter for traceability
