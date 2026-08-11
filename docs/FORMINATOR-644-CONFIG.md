# Forminator 644 — configuration target

This document is the source-of-truth checklist for the live WordPress Forminator form. It does **not** change WordPress by itself.

## Verification snapshot — 11 August 2026

A fresh `Copy outerHTML` capture of the published form was inspected. The live form is `forminator-module-644`.

### Production decision update

The business requirement is that **English is the default translation language**. The office handles approximately 95% of its work in English, so English should remain preselected in the language field. This supersedes the earlier recommendation to require an active language selection.

The supplied browser markup confirms that the rendered Select2 control currently displays `انگلیسی` as selected:

```html
<span class="select2-selection__rendered" ... title="انگلیسی">انگلیسی</span>
```

This snippet confirms the visible selected state, but does **not** by itself confirm the underlying `<option value="...">` for English. The underlying option values should therefore still be verified in the next full outerHTML capture.

### Result: READY FOR NEXT VERIFICATION CAPTURE

The form should not yet be considered ready for final submission testing until the underlying language values and approved urgency wording are confirmed in the published HTML.

## Current live structure observed in the captured HTML

1. `name-1` — نام و نام خانوادگی — optional
2. `phone-1` — تلفن — required
3. `select-1` — زبان مقصد ترجمه — required
4. `upload-1[]` — ارسال مدارک / آپلود اسکن ها — required, multiple files
5. `radio-1` — نوع تاییدات — required
6. `radio-2` — فوریت — optional
7. `textarea-1` — توضیحات در صورت نیاز — optional, max 180 characters

The upload field accepts multiple files. The captured markup reports an 8 MB per-file limit and allows PDF, JPG, JPEG, and PNG.

## Send Documents menu structure

The Send Documents area now has two submenu destinations:

1. **مدارک شخصی، مهاجرتی و تحصیلی** — for individual documents and personal/migration/academic cases.
2. **ارسال پروژه‌های شرکتی و سازمانی** — for corporate and organizational translation projects.

These destinations should remain distinct in navigation and should not be forced into one generic submission flow when the page content and lead qualification differ.

## Language field — approved production configuration

Use these customer-facing options with unique machine-readable values:

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

The field remains **required**, and **انگلیسی is intentionally preselected** as the production default because it represents the office's dominant workload. Do not remove the English default unless the business requirement changes.

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

## Final test gate

Do not merge the send-documents PR until a fresh published HTML capture confirms all of the following:

- every language has a unique value;
- `فرانسوی` no longer submits `روسی`;
- English is intentionally preselected;
- the underlying English option value is `english`;
- urgency is optional;
- urgency labels are exactly the approved three choices;
- certification remains required;
- upload remains multiple-file;
- upload remains restricted to PDF/JPG/JPEG/PNG;
- radio inputs remain native Forminator radios and selectable;
- the two Send Documents submenu destinations point to the intended pages/forms;
- no customer data or uploaded files are committed to GitHub.

## Important: what is NOT changed here

This specification does not change the live WordPress Forminator form. The actual edits must be made in WordPress → Forminator → Form 644, then the published HTML should be inspected again.
