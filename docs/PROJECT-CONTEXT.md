# TarjomeMalek — Project Context

This file is a durable project-context reference for future work on the TarjomeMalek website. It is intentionally limited to project, design, UX, and technical decisions; secrets, credentials, customer data, and private personal information must never be stored here.

## Brand
- Brand/site: دفتر ترجمه رسمی ملک (TarjomeMalek)
- Positioning: premium, trustworthy, conversion-focused official translation office.
- Visual direction: elegant, minimalist, professional; navy + gold + white is the preferred visual language.
- The preferred logo/icon direction comes from the previously developed Elegant Navy and Gold branding work.
- Do not redesign the preferred logo/icon unless explicitly requested. Prefer cleaning, standardizing, and reusing the approved mark.

## Website/design preferences
- Mobile-first: most customers are expected to use mobile.
- Conversion-focused CTAs and forms; avoid oversized/heavy hero sections.
- HTML text should remain real HTML for SEO/accessibility rather than text embedded in images.
- Prefer clean, restrained premium styling over decorative effects.
- Spectra Block Settings currently has practical precedence over the site's Additional CSS in the user's WordPress setup. Use block-specific settings only when appropriate; global/shared behavior should be handled globally rather than requiring repetitive per-block edits.
- WordPress/Blocksy/Spectra compatibility matters for front-end assets.

## Corporate terminology
- For B2B marketing and service descriptions, prefer the Persian term **شرکتی** over **سازمانی**.
- Avoid calling customer document work a «پروژه» when a simpler term such as «مدارک» is appropriate.

## Source-control workflow
- GitHub repository: `majid3m-design/tarjomemalek`
- Default branch: `main`
- Keep GitHub lightweight: it is a project-memory/source-control layer, not a second WordPress installation.
- Reusable front-end assets belong under `assets/`; durable project decisions belong under `docs/`.
- Never commit WordPress credentials, API keys, form submissions, customer documents, passwords, or other secrets/PII.

## Current site reference
- The authoritative current public page list is maintained in `docs/SITE-MAP.md`.
- The current live site has 9 URLs in the Rank Math XML sitemap.
- Older Persian slugs exist in Google's index from the earlier site structure; they are historical unless explicitly revalidated.

## Working priority
The project should prioritize customer acquisition, conversion, and SEO over unnecessary infrastructure work. GitHub documentation should remain only as detailed as needed to make future work accurate and safe.
