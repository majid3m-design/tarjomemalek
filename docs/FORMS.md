# TarjomeMalek — Forms Baseline

Last verified: 2026-08-14

This document records only durable, non-sensitive information needed to understand the site's lead/document-submission flows. Never store customer submissions, credentials, API keys, or private documents here.

## Current form-related components

- Everest Forms has been used for document-submission flows; the known earlier form reference is Everest Form ID 20.
- Forminator is currently used for the corporate document-upload form.
- The site is mobile-first; form simplicity and reliable document upload are high-priority conversion requirements.

## Corporate / B2B form baseline

The current corporate form concept includes:

- First name
- Last name
- Phone (required)
- Target translation language (required)
- Scanned document upload (required)
- Certification / approval type
- Delivery deadline / urgency
- Description when needed
- Submit

Current terminology rule: use «شرکتی» rather than «سازمانی» in B2B marketing and service copy.

## Known implementation history

- Multiple-file upload is important for document-submission flows.
- A previous Forminator issue involved radio-button selection on the published page.
- A previous mixed-content/CSS loading issue affected Forminator styling.
- Spectra block-specific settings can override global Additional CSS in the current WordPress setup.

## Next form work

Before changing a live form, verify the current published form, its fields, upload behavior, notifications, mobile rendering, and destination workflow. This document is a baseline, not a substitute for checking the live configuration.
