# VigWire Labs Production Routing Contract

This document is the standing production guardrail for the VigWire Labs main site.

## Current production boundary

- `vigwirelabs.com` serves the VigWire Labs experience.
- `vigwirelabs.ca` redirects to `vigwirelabs.com`.
- The corporate main-site repository owns the bare-root landing page at `/`.
- VIGscope and its existing production request families remain separate protected behavior.

## Root-only rule

Main-site work may change the response and assets used by the bare-root corporate landing page.

It must not casually alter, replace, intercept, or break any other existing request family. Protected behavior includes, at minimum:

- `/vigscope` and VIGscope application routes.
- Report IDs and report links.
- Compact/short links.
- API routes.
- Existing asset routes used by other applications.
- Scheduler and automated-task handling.
- Existing Worker behavior outside the reviewed main-site scope.

Any change to those families requires separate review and explicit approval.

## Infrastructure guardrail

A main-site visual/content change does not authorize DNS, Cloudflare Worker architecture, scheduler, API, report-routing, compact-link, or unrelated production-routing changes.

When infrastructure work is required, preserve an immediate rollback path and verify protected routes before and after deployment.

## Program ownership

Page-specific implementation and assets belong to the program that owns the page:

- The VigWire Labs main-site repository owns corporate/main-page assets.
- VIGscope owns VIGscope, the 19th Hole, Hotlines, Syndicates, and their related page-specific/share assets.
- TenPlay owns TenPlay and its related page-specific/share assets.

Cross-program assets should not be duplicated into this repository unless the corporate page itself directly uses them.

## Change discipline

Before a production-affecting change:

1. Identify the exact route or asset family being changed.
2. Confirm that it falls inside the owning repository's boundary.
3. Preserve all unrelated production request families.
4. Make the smallest scoped change possible.
5. Verify the intended page and protected routes after deployment.
6. Retain a known rollback point.
