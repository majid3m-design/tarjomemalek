# TarjomeMalek — Project Status

Last verified: 2026-08-14

## Current baseline

- Repository: `majid3m-design/tarjomemalek`
- Default branch: `main`
- Website platform: WordPress
- Current public sitemap: 9 URLs — see `docs/SITE-MAP.md`
- Current Google indexed-page baseline supplied from Search Console: 13 URLs, including legacy Persian URLs
- SEO plugin generating sitemap: Rank Math
- Important form components: Everest Forms and Forminator
- Design direction: premium, minimalist, mobile-first, conversion-focused
- Brand palette: white / navy / gold

## Purpose of this repository

This is a lightweight project memory and source-control layer for TarjomeMalek. It is not intended to become a second copy of the entire WordPress installation.

The repository should preserve only information that is useful for:

1. Understanding the current project quickly.
2. Making future website/design/SEO changes safely.
3. Preserving important reusable front-end assets and code.
4. Supporting future migration planning without storing secrets or customer data.

## Current reference documents

- `docs/PROJECT-CONTEXT.md` — durable project/design decisions.
- `docs/SITE-MAP.md` — authoritative current URLs and known legacy URLs.
- `docs/SEO.md` — current SEO/Search Console baseline and audit priorities.
- `docs/FORMS.md` — durable form structure and implementation notes.

## Current site source

`site/pages/homepage.html` currently contains the approved front-end homepage prototype/source available in this repository. Other live WordPress pages have not yet been imported into GitHub and should not be assumed to exist here.

## Current priority

Complete only the minimum GitHub project memory needed for reliable future work. Then move the main effort to SEO and customer acquisition / traction.

## Explicitly out of scope for now

- Full WordPress mirror in GitHub
- Full database backup in Git
- Detailed documentation of every plugin setting
- Complex deployment automation
- Full design-system documentation
- Automated WordPress restoration

Real WordPress backups and migration procedures should be handled separately when justified by the project's needs.

## Safety boundary

Never commit WordPress credentials, API keys, customer submissions, uploaded customer documents, passwords, or other secrets/PII.
