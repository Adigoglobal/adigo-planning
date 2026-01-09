# CodeSpring — Canonical Responsive Web Design Instructions

Applies to: Web Application (Public + Authenticated)
Targets: Mobile Web (iOS Safari, Android Chrome), Tablet, Laptop, Desktop
Priority: Mobile Web FIRST (non-negotiable)

1. Core Principle (Must Be Followed)
The web app must be fully usable on mobile browsers without relying on the native app. Mobile web is not a degraded preview. It must support onboarding, authentication, forms, dashboards, payments, settings, consent flows.

2. Responsive Strategy (Mobile-First)
- Design/render mobile first; progressively enhance
- Desktop extends mobile; never shrink desktop UI for mobile

3. Breakpoints (Canonical)
- ≤360px small phones; 361–430 phones; 431–600 large phones; 601–768 tablet portrait; 769–1024 tablet landscape; 1025–1440 laptop; ≥1441 max-width constrained

4. Layout Rules
- Mobile: single column; no sidebars; no multi-col tables; no horizontal scroll
- Tablet: up to 2 columns; card grids; tables only if scrollable/collapsible
- Desktop: multi-column; sidebar allowed; tables with pagination, truncation, sticky headers

5. Typography
- Base ≥16px (never <14px); mobile CPL 35–65; enforce max-width on desktop; wrap long text/URLs/IDs

6. Touch & Interaction
- Tap targets ≥44×44px; spaced buttons/links; no hover-only interactions; inputs scroll into view; avoid fixed elements blocking inputs

7. Tables → Mobile
- Do not use dense desktop tables; convert to cards/expandables/key-value lists; horizontal scroll with sticky first column is last resort

8. States (All screens)
- Loading (skeleton preferred), Empty (instructional + CTA), Error (retry), Success (confirmation), Disabled (during async)

9. Performance & Stability
- Avoid CLS; reserve image space; prefer skeletons; handle slow/flaky networks with graceful feedback

10. Safe Area & Quirks
- iOS: respect notch; use dynamic viewport units; test fixed headers/scroll
- Android: ensure address bar collapse doesn’t break layout; fixed footers remain tappable

11. Dark Mode
- AA contrast; no pure black unless designed; no auto-tinting logos/images

12. Accessibility
- Semantic HTML; labeled inputs; announce errors; visible focus; no color-only indicators; support 200% zoom without layout break

13. Testing Requirements
- Mobile: iOS Safari, Android Chrome
- Tablet: iPad Safari, Android Chrome
- Desktop: Chrome, Safari, Firefox

14. Definition of Done — Responsive Web
- Works on mobile web (no horizontal scroll)
- Fully usable via touch; no hidden hover-only actions
- Forms usable with on-screen keyboard
- All states implemented
- Passes dark mode and accessibility checks on small screens

Final Enforcement
- Treat mobile web as first-class. Desktop must never dictate mobile. Features that break on iOS or Android mobile browsers must be rejected.
