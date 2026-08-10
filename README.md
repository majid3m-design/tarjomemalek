# TarjomeMalek

**دفتر ترجمه رسمی ملک | دارالترجمه ۱۰۳۲ تهرانپارس**

Repository for the website redesign, reusable front-end assets, documentation, and deployment-ready code of TarjomeMalek.

## Project goals

- Keep the website code modular and version-controlled.
- Separate reusable HTML/CSS/JavaScript from WordPress-specific implementation details.
- Make design changes reviewable through GitHub commits and pull requests.
- Preserve a clear source of truth for the current website structure.
- Support a mobile-first, conversion-focused service website.

## Repository structure

```text
.
├── .github/
│   └── workflows/       # Automated validation
├── assets/              # Reusable brand and design assets
├── docs/                # Project decisions and technical documentation
├── site/                # Front-end source files and page prototypes
│   ├── assets/
│   │   ├── css/
│   │   ├── js/
│   │   └── images/
│   └── pages/
├── .gitignore
└── README.md
```

## Working model

`main` is the stable branch. Feature work should normally use branches such as:

```text
agent/homepage-hero
agent/send-documents-form
agent/service-pages
agent/seo-structure
```

Changes should be reviewed through pull requests before being merged into `main`.

## Important boundary

This repository is the source-control layer for the website project. WordPress runtime configuration, plugin settings, form data, credentials, and customer information must **not** be committed here.

## Current status

Initial repository bootstrap. The next commits establish the validation workflow, front-end source structure, documentation, and reusable asset directories.
