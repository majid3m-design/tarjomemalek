# TarjomeMalek — Current Project State

Last verified: 2026-08-21

## Website

- Platform: WordPress
- Current public sitemap: 9 URLs — see `docs/SITE-MAP.md`
- SEO sitemap: Rank Math XML Sitemap
- Google Search Console baseline supplied by the project owner: 13 indexed URLs, including legacy Persian URLs
- Current primary objective: increase qualified leads and translation orders

## Current pages

The authoritative current URL list is maintained in `docs/SITE-MAP.md`. Do not infer current page names from older conversation history.

## Services page

- Current public URL: `/services/`
- Current source snapshot: `site/pages/services.html`
- Internal links were corrected/verified on 2026-08-21.
- Current service destinations: `/guide-certified-translation/`, `/syllabus-translation/`, `/corporate-translation/`, `/interpretation/`.
- Services page also links to `/send-documents/` and `/contact-us/` for conversion actions.

## Forms

- Everest Forms and Forminator are important form components.
- Durable form structure and known implementation notes are maintained in `docs/FORMS.md`.
- Never store customer submissions or uploaded documents in this repository.

## SEO baseline

- Current sitemap contains 9 URLs.
- Several older Persian URLs remain visible in Google's indexed-page report.
- At least one tested legacy Persian URL currently returns 404.
- Legacy redirects are not currently a priority because the site is very new and there is no known meaningful traffic/value from those URLs.
- Detailed SEO notes and the baseline supplied from Search Console are maintained in `docs/SEO.md`.

## Design / UX

- Premium, restrained, professional visual direction.
- Navy / gold / white brand language.
- Mobile-first and conversion-focused.
- Real HTML text is preferred over text embedded in images.
- Avoid unnecessarily oversized or decorative sections.

## GitHub role

This repository is a lightweight external project memory and source-control reference. Its primary purpose is to prevent important project state and decisions from being lost or misremembered.

It may also preserve selected reusable assets or source files when they are useful. It is **not** intended to reproduce the whole WordPress installation or serve as the primary WordPress backup.

## Current GitHub scope

Keep only what is useful for:

1. Understanding the current project quickly.
2. Making future SEO/design/content changes safely.
3. Preserving durable decisions.
4. Keeping selected reusable assets available for future work.

Do not expand the repository merely for completeness.

## Current priorities

1. SEO audit and correction of high-value issues.
2. Conversion and customer-acquisition improvements.
3. Traction measurement across organic search, Google Maps, and advertising channels.
4. Update this file only when a material project state or priority changes.

## Out of scope for now

- Full WordPress mirror
- Full HTML/CSS archive of every live page
- Database backup in Git
- Detailed plugin-setting archive
- Deployment automation
- Automated WordPress restoration

## Safety boundary

Never commit credentials, API keys, passwords, customer submissions, uploaded customer documents, or other secrets/PII.
