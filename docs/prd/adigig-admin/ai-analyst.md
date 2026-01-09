# AdiGig AI Analyst (Server-only OpenAI)

Files
- apps/web/lib/adigig/ai/prompt.ts (system prompt)
- apps/web/lib/adigig/ai/tools.ts (tool schemas)
- apps/web/app/api/adigig/ai/route.ts (POST; SSE streaming; RBAC; audit; rate limit)

Policies
- No client keys; mask PII; avoid raw GPS; include References line; use downsampled routes when needed
