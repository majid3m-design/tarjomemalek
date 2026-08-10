# Send Documents page

## Purpose

The source page provides the conversion-focused layout around the live WordPress form. The form plugin remains a WordPress runtime dependency and is not duplicated as application code here.

## Current integration

The page reserves `#document-upload-form` for the live Forminator form and currently references Forminator form ID `644`.

## Verified Forminator 644 markup

The live HTML supplied from WordPress confirms the following field structure:

1. `name-1` — نام و نام خانوادگی — optional
2. `phone-1` — تلفن — required
3. `select-1` — زبان مقصد ترجمه — required, rendered by Select2
4. `upload-1[]` — ارسال مدارک / آپلود اسکن ها — required, multiple upload
5. `radio-1` — نوع تاییدات — required
   - مهر مترجم رسمی قوه قضائیه
   - مهر مترجم با تایید دادگستری و خارجه
   - مطمئن نیستم
6. `radio-2` — تعیین فوریت — optional
   - فوریت آنی امروز (حتما با دفتر تماس بگیرید)
   - فوریت تا فردا
   - فوریت تا سه روز دیگر
7. `textarea-1` — توضیحات در صورت نیاز — optional, maximum 180 characters
8. Forminator submit button — `button.forminator-button-submit`

The upload control accepts multiple files and exposes an 8 MB per-file limit in the supplied markup. Allowed extensions are shown as PDF, JPG, JPEG, PNG.

## CSS integration rule

The page stylesheet is now scoped to the real Forminator 644 structure, especially:

- `#forminator-module-644`
- `.forminator-field-select .select2-container.forminator-select`
- `.forminator-multi-upload`
- `.forminator-field-radio .forminator-radio`
- `.forminator-button-submit`

The CSS deliberately does not hide, disable, or reposition the actual radio inputs. Forminator's own radio bullet and input remain part of the control so the previous radio-selection failure is not reintroduced by the page stylesheet.

## Data-quality item found during inspection

The supplied live markup contains apparent value/label mismatches in the language selector. In particular, the option displayed as `فرانسوی` has a value of `روسی`, while the option displayed as `روسی` also has a value of `روسی`. The Spanish and German entries also use inconsistent internal values compared with their labels.

This is a **form configuration issue**, not a CSS issue. It should be corrected inside Forminator before relying on the submitted language value for processing or reporting.

## Current form decisions

The current project history establishes these UX requirements:

- Mobile-first because most customers use mobile.
- Keep the hero compact so the form is visible quickly.
- Ask only for information needed to quote and process the translation.
- Support multiple uploaded documents in one upload area where the active Forminator configuration permits it.
- Urgency is optional and uses the practical choices: `تا سه روز`, `تا فردا`, `امروز (حتماً تماس بگیرید)`.
- Cost should not be displayed as a fixed amount before the documents are reviewed.

## Important boundary

Do not commit customer submissions, uploaded documents, email credentials, SMTP credentials, WordPress configuration, or plugin-generated runtime files to this repository.
