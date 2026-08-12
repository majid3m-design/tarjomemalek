# TarjomeMalek — Project Context

This file is a durable project-context reference for future work on the TarjomeMalek website. It is intentionally limited to project, design, UX, and technical decisions; secrets, credentials, customer data, and private personal information must never be stored here.

## Brand
- Brand/site: دفتر ترجمه رسمی ملک (TarjomeMalek)
- Positioning: premium, trustworthy, conversion-focused official translation office.
- Visual direction: elegant, minimalist, professional; navy + gold + white is the preferred visual language.
- A previously created concept named **Elegant Navy and Gold Translation Branding Sheet** contains the currently preferred logo/icon direction.
- Do not redesign the preferred logo/icon unless explicitly requested. Prefer extracting, cleaning, vectorizing, and standardizing the existing mark.

## Logo and favicon workflow
- Treat the existing logo artwork/mockup as the source reference.
- Goal: produce a clean, standard vector master and derive all web assets from it.
- Preferred master format: SVG/vector; keep a source/master version when possible.
- Required derived assets may include: full logo, symbol-only mark, monochrome/white variants, favicon 512px, 192px, and 32px PNGs.
- Favicon should use the symbol/mark rather than the full wordmark when legibility requires it.
- Do not simply crop a mockup and call it a logo; remove mockup context and create a genuine vector result.
- For this task the user wants a free workflow and does not want to redraw the logo from scratch.
- Current candidate workflow: Photopea for browser-based raster/vector conversion; Inkscape as the free desktop vector cleanup/export tool. Avoid assuming paid Adobe software is available.

## Website/design preferences
- Mobile-first: most customers are expected to use mobile.
- Conversion-focused CTAs and forms; avoid oversized/heavy hero sections.
- HTML text should remain real HTML for SEO/accessibility rather than text embedded in images.
- Prefer clean, restrained premium styling over decorative effects.
- Spectra Block Settings currently has practical precedence over the site's Additional CSS in the user's WordPress setup. Use block-specific settings only when appropriate; global/shared behavior should be handled globally rather than requiring repetitive per-block edits.
- WordPress/Blocksy/Spectra compatibility matters for front-end assets.

## Corporate terminology
- For B2B marketing and service descriptions, prefer the Persian term **شرکتی** over **سازمانی**.

## Source-control workflow
- GitHub repository: `majid3m-design/tarjomemalek`
- Default branch: `main`
- Use feature branches for meaningful changes and keep `main` stable.
- Reusable front-end assets belong under `assets/`; documentation and durable project decisions belong under `docs/`.
- Never commit WordPress credentials, API keys, form submissions, customer documents, or other secrets/PII.

## Current task
The immediate design task is to turn the preferred logo/icon from the **Elegant Navy and Gold Translation Branding Sheet** into a clean web-ready favicon/icon without redesigning it. The user currently has an upload limitation in ChatGPT, so workflows should not depend on uploading the mockup into the chat. If the user provides a local file, guide them through Photopea/Inkscape or use an accessible project asset when available.
