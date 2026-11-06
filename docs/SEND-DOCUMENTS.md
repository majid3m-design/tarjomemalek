# Send Documents page

Last verified: 2026-11-06

## Purpose

The page provides the conversion-focused layout around the live WordPress form. The form plugin remains a WordPress runtime dependency and is not duplicated as application code here.

## Current integration

- Public URL: `/send-documents/`
- WordPress page ID: 141
- Live Forminator form ID: 644
- The page reserves `#document-upload-form` for the live form integration.

## Forminator 644 — live field map

The current rendered form includes:

1. نام و نام خانوادگی
2. تلفن — required
3. زبان مقصد ترجمه — required (English, Spanish, German, Turkish, Italian, Chinese, Arabic, and other)
4. ارسال مدارک / آپلود اسکن‌ها — required; multiple files supported; per-file limit shown by the live form is 8 MB
5. نوع تأییدات
6. تعیین فوریت — optional
7. توضیحات در صورت نیاز — optional, 180-character limit
8. ارسال

The WordPress/Forminator configuration remains authoritative for validation, upload limits, field options, notifications, and submission storage.

## Submission/loading feedback

The live Forminator default-design CSS uses `.forminator-response-message.forminator-loading::before` for its loading glyph. The first custom CSS attempt targeted form 811 and a paragraph pseudo-element; neither matched the actual loading indicator on live form 644.

The matching CSS has now been added to the GitHub source file `site/assets/css/send-documents.css`. A corresponding WPCode CSS snippet has been created on the site but remains disabled pending owner review and activation. Do not describe the loading UI change as live until the snippet is enabled and visually verified.

## UX decisions

- Mobile-first because most customers use mobile.
- Keep the hero compact so users reach the form quickly.
- Ask only for information needed to quote and process the translation.
- Keep the upload experience simple and allow multiple documents in one upload area where the active Forminator configuration permits it.
- Keep urgency optional; the practical choices are three urgency levels.
- Do not display a fixed translation price before the documents are reviewed.
- Do not introduce a separate document-type field unless the live business process requires it.

## Important boundary

Do not commit customer submissions, uploaded customer documents, email credentials, SMTP credentials, WordPress configuration, plugin-generated runtime files, or secrets.
