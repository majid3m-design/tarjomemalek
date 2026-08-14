# TarjomeMalek

**دفتر ترجمه رسمی ملک | دارالترجمه ۱۰۳۲ تهرانپارس**

This repository is a lightweight external project memory and source-control reference for the TarjomeMalek website.

## Purpose

- Preserve the current project state and durable decisions outside conversational memory.
- Keep the authoritative current URL/page reference.
- Record important SEO, form, design, and implementation notes.
- Preserve selected reusable brand/design assets when useful.
- Provide a reliable reference for future website, SEO, design, and marketing work.

## What this repository is NOT

- It is not a second copy of the entire WordPress website.
- It is not the primary WordPress database backup.
- It is not a complete archive of every plugin setting or media file.
- It is not an automated WordPress restoration system.

## Repository structure

```text
.
├── assets/              # Selected reusable brand/design assets
├── docs/                # Project memory, status, decisions, SEO and forms
├── site/                # Selected source/prototypes when genuinely useful
├── .gitignore
└── README.md
```

## Key documents

- `docs/PROJECT-STATUS.md` — current project state and priorities.
- `docs/PROJECT-CONTEXT.md` — durable project/design context.
- `docs/DECISIONS.md` — important decisions and their rationale.
- `docs/SITE-MAP.md` — authoritative current URLs and known legacy URLs.
- `docs/SEO.md` — SEO/Search Console baseline and notes.
- `docs/FORMS.md` — durable form structure and implementation notes.

## Working principle

Keep this repository deliberately small. Add information when it improves accuracy, continuity, safety, or future reuse — not merely for completeness.

The main business priorities are SEO, conversion, traction, and customer acquisition. GitHub infrastructure should not consume disproportionate project time.

## Security boundary

Never commit WordPress credentials, API keys, passwords, customer submissions, uploaded customer documents, private personal information, or other secrets/PII.
