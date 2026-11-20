# دروازه انتخاب مجری و ارزیابی معماری TMOS — Antigravity Free

- تاریخ: 2026-11-20
- وضعیت: نامزد اصلی برای آزمون؛ هنوز مجری قطعی توسعه گسترده نشده
- مدیر پروژه/عامل چهارم: ChatGPT
- مالک محصول: دفتر ترجمه رسمی ملک

## 1. تصمیم موقت انتخاب مجری

**نامزد اصلی: Google Antigravity در طرح رایگان Individual ($0/month).**

دلیل انتخاب:
- محصول فعلی گوگل برای توسعه عامل‌محور است و هم App، هم CLI و هم IDE extension دارد.
- امکان اجرای چندعامل پس‌زمینه، subagents، ابزار مرورگر و اجرای وظایف زمان‌بندی‌شده دارد.
- طرح رایگان سهمیه پایه عامل را هفتگی بازنشانی می‌کند.
- Git و بازبینی تغییرات/تست‌ها در محیط توسعه قابل استفاده‌اند.

**محدودیت مهم:** سقف عددی سهمیه رایگان هفتگی در مستندات عمومی عددگذاری نشده است؛ سهمیه بر اساس ظرفیت و پیچیدگی کار مصرف می‌شود و ممکن است تغییر کند. بنابراین هیچ برآورد قطعی برای تعداد تسک یا زمان اتمام پروژه نمی‌دهیم. در روز 2026-11-20، مدل رایگان اصلی قابل اتکا در جدول رسمی مدل‌ها Gemini 3.8 Flash است؛ مدل‌های شریک که قبلاً در Free فهرست شده بودند طبق یادداشت رسمی در 2026-11-18 حذف شده‌اند. مدل‌های قوی‌تر Gemini 4 عمدتاً در طرح‌های پولی هستند.

## 2. سیاست بدون پرداخت اجباری

برای این پروژه:
1. فقط طرح Individual با قیمت $0/month استفاده شود.
2. Google AI Pro/Ultra، دوره آزمایشی با تبدیل خودکار به اشتراک، Cloud billing، Vertex pay-as-you-go، کلید API پولی یا هر سرویس مصرف‌محور فعال نشود.
3. هیچ گزینه AI credit overage یا خرید اعتبار فعال نشود. اگر چنین گزینه‌ای نمایش داده شد، آن را خاموش/رد کن.
4. با رسیدن به سهمیه، کار متوقف و وضعیت در GitHub ذخیره شود؛ ادامه فقط پس از reset رایگان مجاز است. هیچ ارتقایی درخواست یا انجام نشود.
5. در صورت تغییر شرایط Free یا حذف سرویس، توسعه متوقف می‌شود تا مجری جایگزین رایگان دوباره ارزیابی شود؛ هیچ هزینه‌ای بدون تصویب مالک مجاز نیست.

## 3. نامزد جایگزین

**Antigravity CLI (agy)** همان اکوسیستم و حساب/سهمیه Antigravity را به‌صورت ترمینالی در اختیار می‌گذارد؛ جایگزین مستقل سهمیه نیست، اما در صورت مشکل رابط گرافیکی، می‌توان آن را در محیط پشتیبانی‌شده بررسی کرد.

Gemini CLI قدیمی برای حساب‌های رایگان فردی گزینه پشتیبان محسوب نمی‌شود؛ ورود رایگان فردی آن از 2026-06-18 متوقف و کاربران به Antigravity منتقل شده‌اند.

ابزارهای محلی متکی بر مدل‌های Ollama/لوکال فعلاً مجری پشتیبان قابل اتکا برای کل پروژه نیستند؛ سخت‌افزار فعلی کاربر (حدود 12GB RAM و بدون GPU مجزا) برای اجرای مدل‌های کدنویسی بزرگ محدود است. می‌توانند بعداً برای وظایف سبک ارزیابی شوند.

## 4. پیش‌نیاز سیستم

نسخه Desktop رسمی Antigravity برای Windows حداقل Windows 10 نسخه 64-bit می‌خواهد. اگر رایانه مورد استفاده هنوز Windows 7/32-bit باشد، نصب Desktop پشتیبانی نمی‌شود و باید از رایانه/محیط دیگری با سیستم پشتیبانی‌شده استفاده شود. پیش از هر نصب، نسخه و معماری سیستم تأیید شود.

## 5. مرحله اول — فقط ارزیابی معماری (بدون کدنویسی)

مخزن:
https://github.com/majid3m-design/tarjomemalek

فایل‌های اجباری برای مطالعه:
- docs/teamos/README.md
- docs/teamos/PRD.md
- docs/teamos/RFP-V0.3.md
- docs/teamos/UX-WIREFRAME-V0.2.md
- docs/teamos/DECISIONS.md
- docs/teamos/WORKFLOWS.md
- docs/teamos/PRD-REVIEW-V0.2.md
- docs/teamos/VALIDATION-PLAN.md

**مأموریت دقیق:**

You are the senior software architect candidate for TMOS.

Read all files listed above. This is an ARCHITECTURE-ONLY evaluation. Do not implement features, do not create application scaffolding, do not change the main branch, and do not modify existing product requirements.

Create a new branch named "agent/architecture-proposal-v0.1" and deliver one reviewable pull request containing only:
"docs/teamos/ARCHITECTURE-PROPOSAL-V0.1.md"

The report must contain:
1. Requirements and repository gap analysis; identify contradictions and missing decisions.
2. Recommended technology stack with reasons and rejected alternatives.
3. Deployment architecture and realistic hosting/runtime cost assumptions. Separate mandatory cost from optional cost.
4. Data model for customers, requests, receipt/intake events, cases, documents, catalogue prices, order-specific price overrides, pre-invoices, invoice snapshots, payments, delivery, files and audit events.
5. Persian RTL and Jalali-date strategy, Asia/Tehran timezone, holidays, business-day calculation and exact test cases.
6. Invoice calculations and unit tests for all rates in RFP-V0.3.md.
7. Secure authentication and role model: owner, secretary, translator assistant.
8. Offline-first design: local data scope, queued mutations, file handling, conflict resolution, backup/restore and device revocation.
9. PDF generation strategy with A4 layout, multi-page tables, Persian font shaping and visual regression tests.
10. Security/privacy threat model; secrets and bank/payment details must not enter repository, fixtures, logs or screenshots.
11. Phased delivery plan with dependencies, acceptance criteria and rollback/backup steps.
12. Risk register with P0/P1 severity and mitigation.
13. A blunt feasibility verdict: what can be delivered reliably in MVP, what must be deferred, and what is not realistic under zero paid infrastructure.

**Hard constraints:**
- No implementation in this task.
- No paid API, cloud billing, paid plugin, paid font or paid service as a required dependency.
- Do not assume unlimited free hosting or free storage.
- No secret, token, customer data or bank account in code or PR.
- Do not add marketing CRM, lead funnels or sales campaign functionality.
- Do not alter the approved process: official translation is printed on the physical Judiciary letterhead; the office's private letterhead is for unofficial translations only.
- Do not claim real-time collaboration during a total network outage.
- Any unresolved rule must be explicitly labelled assumption/open decision, not silently invented.
- If quota is reached, stop; keep the repository unchanged except for the approved documentation PR, and resume after the free reset. Never ask the owner to upgrade.

## 6. معیار قبولی عامل معماری

- سند معماری تمام 13 موضوع بالا را پوشش دهد.
- هر نیازمندی RFP به راهکار و آزمون قابل ردیابی باشد.
- هزینه اجباری سرویس‌های بیرونی صفر باشد یا صریحاً به‌عنوان مانع MVP اعلام شود.
- مسیر استقرار بدون کارت بانکی/قبض مصرفی اجباری تا حد امکان مشخص باشد.
- فرمول‌ها و تاریخ‌های نمونه با مثال‌های محاسباتی آزمون‌پذیر باشند.
- فقط یک PR مستنداتی ایجاد شود؛ هیچ کد برنامه‌ای تغییر نکند.
- مدیر پروژه/عامل چهارم پیش از تأیید مالک، هیچ مجوز پیاده‌سازی را صادر نکند.

## 7. Prompt کوتاه برای شروع در Antigravity

Select the TMOS repository and use the free Individual plan. Read "docs/teamos/ANTIGRAVITY-ARCHITECTURE-GATE-V0.1.md" and execute only Section 5. First show your plan and wait for approval. Do not code. Do not enable billing or ask for an upgrade. If you reach quota, stop and preserve the current state.
