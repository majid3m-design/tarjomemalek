# TarjomeMalek — Forms Baseline

Last verified: 2026-11-06

Never store customer submissions, uploaded documents, credentials, API keys, or private information in this repository.

## Current form-related components

- Everest Forms 3.6.4 is installed and active; an earlier document-submission reference was Everest Form ID 20.
- Forminator 1.58.4 is installed and active.
- Forminator form ID 644 is the live upload/quote-request form embedded on `/send-documents/`.
- Forminator form ID 811 is a separate published corporate/B2B translation request form.
- Forminator form ID 920 is a draft titled `contact-form`; it is not the live intake form.

## Live form verification (2026-11-06)

The WordPress-rendered page DOM was inspected. The live send-documents form is `#forminator-module-644`, with a Forminator response message container:

```html
<div class="forminator-response-message forminator-error" ...></div>
```

During submission, Forminator applies the `.forminator-loading` state to this response container. The default Forminator theme places its loading glyph with the container's `::before` pseudo-element, while the default message alignment is left-oriented. The previous custom CSS attempt targeted form ID 811 and therefore did not affect the live form 644.

A WPCode CSS snippet was created to style the loading state for Forminator custom forms generally (RTL message, stronger contrast, and an animated brick-orange spinner). The snippet is saved **disabled** and must be reviewed and enabled by the site owner in WPCode before it takes effect. It is not yet a live production change.

## Corporate / B2B form baseline

The B2B form concept includes:

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

## Important boundary

The live WordPress/Forminator instance remains the source of truth for field IDs, validation, upload limits, notifications, anti-spam controls, submission storage, and delivery workflow. GitHub is a project reference, not a duplicate form runtime.
