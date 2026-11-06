# TarjomeMalek — Current Project State

Last verified: 2026-11-06

## Website

- Platform: WordPress 7.1.4, PHP 8.1.34.
- Active theme: Blocksy 2.1.53; update 2.1.61 is available.
- Public sitemap: 9 URLs — see `docs/SITE-MAP.md`.
- SEO plugin: Rank Math 1.0.281 (Free).
- Primary objective: increase qualified leads and translation orders.

## Current public pages

The authoritative current URL list is maintained in `docs/SITE-MAP.md`. Do not infer current page names from older conversation history.

## Forms

- Main online document intake page: `/send-documents/`, WordPress page ID 141, using Forminator form ID 644.
- Separate corporate/B2B request form: Forminator form ID 811.
- Forminator form ID 920 is a draft contact form; it is not the live send-documents form.
- Live form fields and UI notes are in `docs/FORMS.md` and `docs/SEND-DOCUMENTS.md`.

## SEO and technical health

- Rank Math site audit: 78/100 (good); 5 tests OK, 2 failed, 1 warning. Details and limitations are in `docs/SEO.md`.
- XML sitemap is enabled and accessible; robots.txt allows public crawling and declares the sitemap.
- WordPress core, Rank Math, and Forminator checksums verified without mismatches or missing files.
- The Rank Math 404 monitor contains legacy URL hits and routine automated probes; see `docs/SITE-MAP.md` and `docs/SEO.md`.
- SEO metadata coverage, attachment alt metadata, language metadata, and Local SEO coordinates still need attention.

## Design / UX

- Premium, restrained, professional visual direction.
- Navy / gold / white brand language.
- Mobile-first and conversion-focused.
- Real HTML text is preferred over text embedded in images.
- Avoid unnecessarily oversized or decorative sections.

## GitHub role

This repository is a lightweight external project memory and source-control reference. It is **not** a mirror of the WordPress installation, a database backup, or an automated restoration system.

## Current priorities

1. Complete page-level SEO titles, descriptions, and focus keyphrases.
2. Fix Local SEO coordinates and Persian language metadata after verifying the correct values.
3. Add meaningful alt text to the site's media library images.
4. Review legacy 404 paths and decide which deserve 301 redirects.
5. Maintain the reliability and clarity of the online document-intake flow.

## Safety boundary

Never commit credentials, API keys, passwords, customer submissions, uploaded customer documents, private personal information, or other secrets/PII.
