# VigWire Labs Main Site

Corporate landing site for VigWire Labs.

## Day 1 baseline — 2026-09-04

The bare root of `https://vigwirelabs.com/` is the VigWire Labs corporate landing page.

The page currently provides:

- VigWire Labs brand and navigation.
- Product entry points for VIGscope and TenPlay.
- The VigWire Labs crew and supporting brand artwork.
- Contact via `mudwater365@gmail.com`.
- Native/fallback sharing from the VigWire Hotline share control.

VIGscope is entered through `https://vigwirelabs.com/vigscope`. TenPlay remains its own application and deployment, linked from the main page.

## Repository ownership

This repository owns the VigWire Labs corporate/main-site implementation and the assets used directly by that site.

Application-specific material stays with the application that owns the page:

- **VIGscope** owns VIGscope application pages and related identities, including the 19th Hole, Hotlines, Syndicates, and their page-specific/share assets.
- **TenPlay** owns the TenPlay application and its page-specific/share assets.
- **VigWire Labs Main Site** owns only corporate/main-page assets and identities used directly here.

Do not use this repository as a central warehouse for graphics that belong to another VigWire program.

## Production boundary

The main site owns the bare-root landing-page experience only. Existing VIGscope, report, compact-link, API, asset, scheduler, and other production request families are protected and must not be changed as a side effect of main-site work.

See `PRODUCTION-GUARDRAILS.md` for the standing routing contract.

## Visual authority

The approved live homepage implementation and approved production artwork are the current implementation authority. Historical/locked design references remain under `assets/reference/` for comparison and provenance.

Production assets are organized under `assets/`; see `assets/README.md` for the directory contract.
