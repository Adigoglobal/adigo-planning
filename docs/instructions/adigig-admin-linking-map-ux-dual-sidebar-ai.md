# CodeSpring Instruction — AdiGig Admin ↔ Mobile Data Linking + Map UX + Dual-Sidebar Layout + OpenAI Chat

Scope: Admin Dashboard + AdiGig Admin Dashboard + Mobile session ingestion
Goal: Correct user/session linkage; map organized by User → Date/Range → Session; VS‑Code‑style layout (left nav, right AI pane); AI via server proxy.

1) Canonical Data Link
- user_id from Clerk (server-verified); session_id UUID; started_at/ended_at; app_source; route refs; summary stats
- Reject uploads without verified userId
- Admin reads by user/time (users list, user sessions in range, session detail + route)

2) Map UX Restructure
- Default flow: Select User → Select Date (or range) → Select Session → Map + Summary
- Controls: User selector (searchable), Date presets (Today/7/30), Session selector
- Behavior: Empty states; downsampled route fetch on selection; cache lists where safe

3) Dashboard Layout (Both Admins)
- Left vertical sidebar (collapsible), main content, right AI pane (collapsible)
- Menus: Admin vs AdiGig examples; icons optional; collapsed tooltips

4) AI Chat Panel (Both) — Server-only OpenAI
- UI: toggle open/close; chat history per context; context chips (user, session, date range); suggested prompts
- Server: /api/.../ai/chat proxy; RBAC; audit; rate limits; no client keys

5) Cross-Linking
- Admin→AdiGig: “View in AdiGig” (user_id param)
- AdiGig→Admin: link back to Admin user record
- Reuse same sidebar + AI pane components

6) QA Checklist (must pass)
- Mobile↔Admin linking; Map UX states; Layout + AI pane on both; server proxy working; no keys in client; mobile admin basics usable

7) Deliverables
- AdiGig Map Explorer v2 (User → Date → Session flow)
- Unified Admin layout shell (left nav + main + right AI pane) for both dashboards
- Admin-only AI proxy; RBAC + rate limits + minimal audit
- Cross-links between Admin and AdiGig user/session views
