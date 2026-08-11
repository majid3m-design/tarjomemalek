# Forminator 644 — configuration target

This document is the source-of-truth checklist for the live WordPress Forminator form. It does **not** change WordPress by itself.

## Current live structure observed in the captured HTML

The live form is `forminator-module-644`. The captured markup shows:

1. `name-1` — نام و نام خانوادگی — optional
2. `phone-1` — تلفن — required
3. `select-1` — زبان مقصد ترجمه — required
4. `upload-1[]` — ارسال مدارک / آپلود اسکن ها — required, multiple files
5. `radio-1` — نوع تاییدات — required
6. `radio-2` — فوریت — optional
7. `textarea-1` — توضیحات در صورت نیاز — optional, max 180 characters

The upload field accepts multiple files and the captured markup reports an 8 MB per-file limit. Allowed extensions shown by the form are PDF, JPG, JPEG, PNG.

## Send Documents menu structure

The Send Documents area now has two submenu destinations:

1. **مدارک شخصی، مهاجرتی و تحصیلی** — for individual documents and personal/migration/academic cases.
2. **ارسال پروژه‌های شرکتی و سازمانی** — for corporate and organizational translation projects.

These destinations should remain distinct in navigation and should not be forced into one generic submission flow when the page content and lead qualification differ.

## Language field — correction required

The captured HTML contains a data error: the visible option `فرانسوی` currently has the same value as `روسی`. The language values must be unique and semantically match the visible label.

Recommended Forminator options:

| Visible label | Value |
|---|---|
| انگلیسی | english |
| اسپانیایی | spanish |
| آلمانی | german |
| ترکی استانبولی | turkish-istanbul |
| فرانسوی | french |
| ایتالیایی | italian |
| روسی | russian |
| چینی | chinese |
| عربی | arabic |
| سایر زبانها (در توضیحات ذکر شود) | other |

Do not use Persian display labels as data values when a stable English slug is sufficient. The value is the machine-readable data; the label is what the customer sees.

## Urgency field — approved wording

Keep urgency optional. The approved customer-facing choices are:

1. **امروز (حتماً تماس بگیرید)**
2. **تا فردا (روز کاری)**
3. **تا سه روز دیگر (روز کاری)**

Recommended values:

| Visible label | Value |
|---|---|
| امروز (حتماً تماس بگیرید) | today-call |
| تا فردا (روز کاری) | next-business-day |
| تا سه روز دیگر (روز کاری) | within-three-business-days |

The wording deliberately distinguishes business days from calendar days. Do not add translation fees to these options; urgency is used to reserve/qualify the requested delivery timing, not to display pricing.

## Certification field

Keep `radio-1` required with these choices:

1. مهر مترجم رسمی قوه قضائیه — `official-translator-stamp`
2. مهر مترجم با تایید دادگستری و خارجه — `judiciary-and-foreign-affairs`
3. مطمئن نیستم — `not-sure`

The third option is important for conversion: customers should not have to understand the approval process before submitting their documents.

## Important: what is NOT changed here

This specification does not change the live WordPress Forminator form. The actual edits must be made in WordPress → Forminator → Form 644, then the published HTML should be inspected again.

After editing, verify:

- each language has a unique value;
- `فرانسوی` no longer submits `روسی`;
- urgency is optional;
- urgency labels are exactly the approved three choices;
- certification remains required;
- upload remains multiple-file;
- radio inputs remain native Forminator radios and selectable;
- the two Send Documents submenu destinations point to the intended pages/forms;
- no customer data or uploaded files are committed to GitHub.
