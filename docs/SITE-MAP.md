# TarjomeMalek — Current Site Map

Last verified: 2026-11-06

This file is the current reference for the live WordPress site's public page structure. Do not infer current page names or URLs from older conversation history.

## Current sitemap

Rank Math currently reports 9 URLs in the XML page sitemap:

| Page | Current URL |
|---|---|
| Homepage | `/` |
| Corporate translation | `/corporate-translation/` |
| Send documents | `/send-documents/` |
| Syllabus translation | `/syllabus-translation/` |
| Interpretation | `/interpretation/` |
| Services | `/services/` |
| Guide to certified translation | `/guide-certified-translation/` |
| About us | `/about-us/` |
| Contact us | `/contact-us/` |

## Services page internal links

The current `/services/` page links to these public pages:

| Service | Destination |
|---|---|
| Official document translation | `/guide-certified-translation/` |
| Syllabus translation | `/syllabus-translation/` |
| Corporate translation | `/corporate-translation/` |
| Official interpretation | `/interpretation/` |
| Send documents | `/send-documents/` |
| Contact us | `/contact-us/` |

The current source version of the Services page is preserved in `site/pages/services.html`.

## Legacy URLs and 404 monitor (2026-11-06)

Rank Math's 404 monitor reported 38 unique URLs and 76 total hits at the time of inspection. Notable paths:

| Legacy / missing path | Current page / observation | 404 monitor hits |
|---|---|---:|
| `/تماس` | Contact CTA was corrected to use `tel:+989362195750`; canonical contact page is `/contact-us/` | 13 |
| `/ارسال-مدارک` | Current send-documents page is `/send-documents/` | 4 |
| `/payment` | No matching published/draft WordPress page found; destination needs a business decision | 7 |
| `/خدمات-ترجمه-رسمی/` | Current services page is `/services/`; manually tested as 404 on 2026-08-14 | — |

The 404 monitor also contains low-hit requests for common plugin/file/environment probes (e.g. `wp-plain.php`, `alfacgiapi`, `.aws/credentials`, `actuator/env`). These are failed requests recorded as 404s and are not evidence by themselves of a successful intrusion.

## Redirect policy

Rank Math redirection module is enabled but has 0 redirects at this review. Consider 301 redirects for legacy Persian paths when the destination is unambiguous:

- `/تماس/` → `/contact-us/` (the contact CTA itself now uses a telephone link).
- `/ارسال-مدارک/` → `/send-documents/`.

Do not redirect `/payment/` until its intended destination is confirmed. Keep the canonical current page URLs above; do not restore legacy Persian paths as duplicate pages.

## Important rule

The 9 URLs above are the authoritative public page structure for current work. Older page names mentioned elsewhere should be treated as historical unless verified against the live site or this file.
