# TarjomeMalek — SEO Baseline

Last verified: 2026-11-06

## Rank Math audit

- Rank Math SEO 1.0.281 (Free) is active.
- Latest local Rank Math site audit score: **78/100 (good)**.
- Test results: 5 OK, 2 failed, 1 warning (8 total).
- Rank Math's remote audit API was unavailable during the run; local checks did complete.

### Failed / warning checks

- **Focus keywords:** Rank Math reports 8 published pages with no focus keyword. Focus keywords are editorial analysis inputs, not a direct ranking factor by themselves; select them page by page based on the target search intent.
- **Search Console integration:** Rank Math has no Google refresh token and Search Console permission is not granted to Rank Math. Site Kit is installed, but this check does not establish whether Site Kit itself is connected.
- **Site tagline:** WordPress `blogdescription` is empty. Add a concise, accurate tagline if it will be useful to visitors and search engines.

### Crawlability and sitemap

- WordPress `blog_public=1`: the site is not discouraging search-engine crawling.
- Permalink structure: `/%postname%/`.
- Rank Math sitemap module is enabled; sitemap index is accessible at `/sitemap_index.xml`.
- `robots.txt` allows public crawling, disallows only `/wp-admin/`, and declares the sitemap.
- Rank Math reports 9 URLs in its page sitemap.
- Rank Math redirection module is enabled but currently has 0 redirects.

## Database metadata coverage

A read-only query of the 9 published posts/pages found:

- 7 without a custom Rank Math SEO title field (`rank_math_title`).
- 6 without a custom Rank Math meta-description field (`rank_math_description`).

The six pages sampled without a custom description are Contact (199), Services (210), Interpretation (231), About (422), Syllabus Translation (518), and Corporate Translation (547). Missing custom fields do not necessarily mean the rendered page has no title/description: Rank Math may fall back to its configured templates or page excerpts. Review rendered output before writing replacements.

## Image alternative text

The media library has 70 image attachments; all 70 currently have an empty `_wp_attachment_image_alt` value in attachment metadata. This is a metadata coverage finding, not proof that every frontend image is missing an `alt` attribute (some page builders may set alt text separately). Add descriptive alt text where the image conveys useful information; leave decorative images empty.

## Local SEO / language data

- The rendered page schema currently contains placeholder coordinates (`Latitude` / `Longitude`) in the Place entity and a map URL built from those placeholders. Replace them only after verifying the office's actual coordinates, or remove the coordinates/map field if they are not known.
- WordPress site language is `en_US`, and rendered page metadata reports `og:locale=en_US` / `inLanguage=en-US` although the primary page copy is Persian. Review the intended site language before changing it; do not change it blindly if multilingual content is planned.
- The Rank Math Local SEO phone number is configured as `+989362195750`.

## 404 monitor and legacy URLs

At the time of review, Rank Math's 404 monitor reported 38 unique URLs and 76 total hits. The highest-hit entries included:

- Legacy Persian contact path `/تماس`: 13 hits (the page's contact CTA has since been changed to a telephone link).
- Legacy Persian send-documents path `/ارسال-مدارک`: 4 hits; the current canonical page is `/send-documents/`.
- `/payment`: 7 hits; no matching published/draft page was found in the WordPress content query.
- Other single- or low-hit paths include common automated probes for exposed files, old plugins, and environment/configuration paths. A 404 hit means the requested path was not found; it does **not** prove that the server was compromised.

Decide which legacy paths deserve 301 redirects. Do not redirect `/payment` until its intended destination is confirmed. The earlier legacy path `/خدمات-ترجمه-رسمی/` was also manually recorded as a 404 on 2026-08-14.

## File integrity and maintenance

- WordPress core checksum verification: passed (3,338 files; no mismatches, missing files, or unexpected core files).
- Rank Math and Forminator plugin checksums: passed with no mismatches or missing files.
- The all-plugin checksum run also passed for the other installed plugins, except All-in-One WP Migration, which reported four additional files under its `storage/` directory and no mismatched or missing upstream files. Do not delete these storage protection files solely because they are listed as extras.
- WordPress maintenance mode is off.
- No `wp-content/debug.log` was available through the connected read-only file interface. Host-level PHP/web-server error logs were not available in this review, so this is not a confirmation that no server errors exist.
- Available updates at review time: Blocksy 2.1.53 → 2.1.61 and WPVibe 1.20.5 → 1.21.7. They were not applied during this audit.

## Priority order

1. Review and add page-specific SEO titles/descriptions and focus keyphrases.
2. Correct Local SEO placeholder coordinates and review Persian language metadata.
3. Add meaningful alt text to image attachments.
4. Add 301 redirects for confirmed legacy page URLs.
5. Connect Search Console to Rank Math only if Rank Math reporting is desired; Site Kit may separately provide Google data.

Do not change SEO settings, redirect destinations, or business coordinates without checking the correct values first.
