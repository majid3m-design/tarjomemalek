# Send Documents page

## Purpose

The source page provides the conversion-focused layout around the live WordPress form. The form plugin remains a WordPress runtime dependency and is not duplicated as application code here.

## Current integration

The page reserves `#document-upload-form` for the live Forminator form and references Forminator form ID `644`.

## Forminator 644 — current field map

Based on the current Forminator 644 configuration used in the TarjomeMalek project, the page is designed around these fields:

1. نام
2. نام خانوادگی
3. شماره تماس — required
4. زبان مقصد ترجمه — required
5. بارگذاری مدارک اسکن‌شده — required; the active configuration supports multiple files in one upload area
6. نوع تأییدات — required/selected according to the live form configuration
7. تعیین فوریت — optional:
   - `تا سه روز`
   - `تا فردا`
   - `امروز (حتماً تماس بگیرید)`
8. توضیحات در صورت نیاز — optional
9. ارسال

The GitHub source does **not** duplicate these fields as a second application form. The live Forminator instance remains the source of truth for field IDs, validation, upload limits, notifications, and submission handling.

## UX decisions

- Mobile-first because most customers use mobile.
- Keep the hero compact so users reach the form quickly.
- Ask only for information needed to quote and process the translation.
- Keep the upload experience simple and allow multiple documents in one upload area where the active Forminator configuration permits it.
- Keep urgency optional; the practical choices are the three options listed above.
- Do not display a fixed translation price before the documents are reviewed.
- Do not introduce a separate document-type field unless the live business process requires it; the current form already collects the information needed for the initial quotation.

## Live integration boundary

The WordPress/Forminator instance is authoritative for:

- field IDs and names
- required/optional validation
- file types and file-size limits
- multiple-file upload behavior
- email/notification settings
- submission storage
- anti-spam/security controls

GitHub is authoritative for the page shell and presentation layer.

## Important boundary

Do not commit customer submissions, uploaded documents, email credentials, SMTP credentials, WordPress configuration, or plugin-generated runtime files to this repository.

## Verification note

The public WordPress site could not be fetched directly during this review, so the field map above is based on the current Forminator 644 configuration and HTML supplied during the TarjomeMalek implementation work. Before the final production CSS is locked, the live rendered Forminator markup should be inspected once in WordPress so selectors can be tied to the actual field wrappers rather than guessed IDs.