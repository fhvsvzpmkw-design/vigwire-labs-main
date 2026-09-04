# Production Guardrails

Current production infrastructure:

- `vigwirelabs.com` is served through the existing Betting Edge Cloudflare Worker.
- `vigwirelabs.ca` redirects to `vigwirelabs.com`.

No DNS, Worker, scheduler, report-link, API-route, asset-route, compact-link, or production-routing changes are authorized yet.

## Planned cutover

1. Build and preview the landing page independently.
2. Establish and verify `/vigscope`.
3. Preserve report IDs, compact links, API routes, assets, and scheduled handling.
4. Change only the bare-root response.
5. Retain an immediate rollback path.

## Root-only rule

The eventual production landing page may replace only the response for the bare-root pathname `/`. All other existing request families must continue through the existing production handler unless separately reviewed and approved.
