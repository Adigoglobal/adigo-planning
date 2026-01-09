# CodeSpring — AdiGig Admin P0 Plan + DoD + Mindmap Hygiene (Paste-ready)

1) Canonical PRD Bridge
- Use only prdBridge-1767679488284-3nsupd9bv for AdiGig Admin v1. Merge orphans; remove stale edges; add hygiene note.

2) P0 Feature Node
- “AdiGig Admin v1 — UI Wiring + Mapbox + E2E Proof (P0)” with real data for /dashboard, /sessions, /sessions/[id], /users, /users/[id], /settings, /ai

3) Mapbox Tasks
- Read-only token; route polyline from session_route?downsample=medium; perf constraints (small payloads, no lockups)

4) E2E Proof Tasks
- Runbook (mobile→API→admin→map→AI) + Verification Evidence (JSON examples, screenshots/logs, commands)

5) Blocking Checks (30-min red flags)
- Fallback recompute; API RBAC; AI route implemented (no 501) with streaming/tool-calls; session_id stability

6) DoD — Audit Completion Checklist
- Build integrity, schema parity, ingestion/dedupe, aggregation, endpoints, UI, maps, AI, logs/rate limits, docs/env parity, E2E verification
