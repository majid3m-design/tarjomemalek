# Send Documents page

## Purpose

The source page provides the conversion-focused layout around the live WordPress form. The form plugin remains a WordPress runtime dependency and is not duplicated as application code here.

## Current integration

The page reserves `#document-upload-form` for the live Forminator form and currently references Forminator form ID `644`.

## Current form decisions

The current project history establishes these important UX requirements:

- Mobile-first because most customers use mobile.
- Keep the hero compact so the form is visible quickly.
- Ask only for information needed to quote and process the translation.
- Support multiple uploaded documents in one upload area where the active Forminator configuration permits it.
- Urgency is optional and uses the practical choices: `تا سه روز`, `تا فردا`, `امروز (حتماً تماس بگیرید)`.
- Cost should not be displayed as a fixed amount before the documents are reviewed.

## Important boundary

Do not commit customer submissions, uploaded documents, email credentials, SMTP credentials, WordPress configuration, or plugin-generated runtime files to this repository.
