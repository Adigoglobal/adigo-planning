---
title: AdiGig Admin v1 — Backend PRD
featureId: feature-adigig-admin-v1
mindmap:
  bridgeId: prdBridge-1767679488284-3nsupd9bv
  prdId: prdBackend-1767679547687-lk18kt68g
version: 1.0.0
status: draft
owners: ["adigo-api"]
links:
  - type: mindmap
    label: Canonical PRD Bridge
    nodeId: prdBridge-1767679488284-3nsupd9bv
---

Admin Endpoints (admin-only, RBAC)
- GET /v1/adigig/admin/overview
- GET /v1/adigig/admin/sessions
- GET /v1/adigig/admin/sessions/:id
- GET /v1/adigig/admin/sessions/:id/route?downsample=low|medium|high
- GET /v1/adigig/admin/users
- GET /v1/adigig/admin/users/:id

Proxy rule
- Web /api/adigig/admin/* → apps/api with Clerk token; server-side guard again
