# دروازه انتخاب مجری و ارزیابی معماری TMOS — Codex Free Local

- تاریخ: 2026-11-21
- وضعیت: نامزد اول برای آزمون محدود؛ هنوز مجری قطعی توسعه گسترده نیست
- مدیر پروژه/عامل چهارم: ChatGPT
- مالک محصول: دفتر ترجمه رسمی ملک

## 1. تصمیم فعلی

**نامزد اول: OpenAI Codex در طرح رایگان ChatGPT، با اجرای محلی روی لپ‌تاپ.**

دلایل:
- Codex در پلن‌های ChatGPT شامل Free نیز ارائه می‌شود.
- Codex CLI و IDE extension امکان کار روی پوشه/مخزن محلی را دارند.
- کار روی فایل‌های محلی به Codex Cloud نیاز ندارد.
- چون حساب ChatGPT کاربر اکنون در دسترس است، این مسیر پیش از ثبت‌نام در سرویس دیگری قابل آزمون است.

محدودیت‌ها:
- Codex Cloud در پلن Free ارائه نمی‌شود.
- دسترسی/تعداد پیام‌ها، taskها و uploads در Free محدود است و میزان دقیق ثابت یا تضمین‌شده برای کل پروژه نیست.
- اگر سهمیه تمام شود، عامل باید متوقف شود و کار با Git checkpoint قابل ادامه باشد؛ هیچ پرداخت یا ارتقایی مجاز نیست.

مستندات رسمی:
- https://help.openai.com/en/articles/11369540-using-codex-with-your-chatgpt-plan
- https://developers.openai.com/codex/cli/

## 2. سیاست قطعی بدون پرداخت

1. فقط ورود با همان حساب ChatGPT در طرح رایگان.
2. از OpenAI API key، API billing، pay-as-you-go، credit purchase، یا هر حساب مصرف‌محور استفاده نشود.
3. Codex Cloud استفاده نشود؛ این Gate برای Codex local/CLI/IDE روی لپ‌تاپ است.
4. هیچ روش پرداختی برای ادامه کار وارد نشود.
5. اگر سهمیه تمام شد یا پیام Upgrade ظاهر شد، کار متوقف شود؛ باقیمانده کار در branch محلی و commitهای Git حفظ شود.
6. ادامه پس از بازگشت سهمیه رایگان، با خلاصه handoff در GitHub انجام شود.
7. هیچ ابزار یا زیرساختی نباید هزینه ناخواسته ایجاد کند.

## 3. وضعیت سایر نامزدها

### Google Jules — حذف‌شده
کاربر در تست مستقیم خطای عدم ارائه سرویس در منطقه جغرافیایی دریافت کرده است. همچنین طبق وضعیت جاری سرویس، Jules برای کار جدید قابل اتکا نیست. دیگر برای این پروژه وقت صرف نشود.

### Google Antigravity Free — مشروط/تأییدنشده
Antigravity Free از نظر قابلیت عامل‌محور مناسب به نظر می‌رسد، اما Google FAQ می‌گوید کشور مرتبط با حساب باید در فهرست جغرافیایی پشتیبانی‌شده باشد. دسترسی آن برای این کاربر هنوز آزمایش نشده و نباید مجری قطعی فرض شود.
- FAQ: https://antigravity.google/docs/faq
- Pricing: https://antigravity.google/pricing
- تا وقتی ورود قانونی و رسمی حساب خود کاربر موفق نشده، نصب و تنظیمات طولانی انجام نشود.
- VPN نباید به‌عنوان راه تضمینی یا روش دور زدن محدودیت جغرافیایی پیشنهاد شود.

### GitHub Copilot Free — پشتیبان محدود
پلن رایگان شامل 2,000 code completions در ماه و مقدار محدود chat/agent usage است. Agent mode در ویرایشگر و CLI وجود دارد؛ اما Copilot Cloud و واگذاری کار به عامل ابری برای ساخت PR در پلن Free شامل نمی‌شود.
- Pricing: https://github.com/features/copilot/plans
- مناسب برای کارهای محدود، اصلاح و تکمیل کد؛ هنوز به‌عنوان مجری مستقل کل TMOS تأیید نشده است.

### Local LLM / Ollama — ابزار کمکی، نه مجری اصلی فعلی
با توجه به سخت‌افزار گزارش‌شده قبلی (حدود 12GB RAM و Intel UHD بدون GPU مجزا)، مدل محلی کوچک می‌تواند برای توضیح/اصلاحات محدود کمک کند، اما برای معماری و توسعه عامل‌محور کل سامانه، فعلاً توان کافی آن اثبات نشده است.

## 4. دو محیط کاری

- لپ‌تاپ پشتیبانی‌شده: محل توسعه، اجرای Codex و Git.
- دسکتاپ Windows 7: محیط مقصد آزمون محصول نهایی؛ نه محیط اجرای Codex.
- سازگاری محصول با Firefox 115 ESR در RFP و Gate معماری ثبت شده است و باید جداگانه آزموده شود.

## 5. مأموریت اول — ارزیابی معماری، بدون کدنویسی

Repository:
https://github.com/majid3m-design/tarjomemalek

ابتدا این اسناد را بخوان:
- docs/teamos/README.md
- docs/teamos/PRD.md
- docs/teamos/RFP-V0.3.md
- docs/teamos/UX-WIREFRAME-V0.2.md
- docs/teamos/DECISIONS.md
- docs/teamos/WORKFLOWS.md
- docs/teamos/PRD-REVIEW-V0.2.md
- docs/teamos/VALIDATION-PLAN.md
- docs/teamos/ANTIGRAVITY-ARCHITECTURE-GATE-V0.1.md

Prompt for Codex:

You are a senior software architect candidate for TMOS.

This is an architecture-only evaluation. Read the project documents listed in the task. Do not implement code, create application scaffolding, install project dependencies, or change the main branch.

Work in a new local branch named "agent/codex-architecture-proposal-v0.1". Produce exactly one document:
"docs/teamos/ARCHITECTURE-PROPOSAL-V0.1.md"

The report must include:
1. Requirements and repository gap analysis; contradictions and missing decisions.
2. Recommended stack and rejected alternatives.
3. Deployment architecture and realistic mandatory/optional infrastructure cost.
4. Data model for customers, requests, receipt/intake events, cases, documents, catalogue prices, order-specific price overrides, pre-invoices, invoice snapshots, payments, delivery, files and audit events.
5. Persian RTL and Jalali-date strategy, Asia/Tehran timezone, official holidays and business-day calculations with exact test cases.
6. Invoice calculations and unit tests for every rate in RFP-V0.3.md.
7. Authentication and role permissions for owner, secretary and translator assistant.
8. Offline-first approach: local data scope, mutation queue, files, conflict resolution, backup/restore and device revocation.
9. A4 Persian PDF generation, multi-page layout, font shaping and visual regression tests.
10. Security/privacy threat model; secrets, bank data and client records must not enter code, fixtures, logs or screenshots.
11. Phased implementation plan, dependencies, acceptance criteria and rollback.
12. P0/P1 risk register.
13. Windows 7 / Firefox 115 ESR compatibility matrix for critical UX, IndexedDB, service worker, file upload/download, PDF and printing.
14. Blunt feasibility verdict: reliable MVP, deferred features, and features not realistic with zero paid infrastructure.

Hard constraints:
- No implementation in this task.
- No API key, billing, paid service, paid font or unexpected expense.
- No Codex Cloud; local work only.
- No secrets or private client/bank data in files or logs.
- No marketing CRM or lead funnels.
- Preserve the official Judiciary physical-letterhead workflow; private office letterhead remains for unofficial translations only.
- Never claim real-time collaboration during a total network outage.
- Mark assumptions and open decisions; do not silently invent business rules.
- Stop at usage limit and preserve all work using Git commits; never ask the owner to upgrade.

After preparing the document, run markdown/link consistency checks only if they require no paid service. Do not modify application files. Show the document and a summary of its recommendations to the project owner. Do not create or push a PR unless asked; the project manager will review it first.

## 6. معیار قبولی Gate

- سند معماری تمام 14 سرفصل را پوشش دهد.
- هر نیاز RFP به راهکار و آزمون قابل ردیابی باشد.
- هزینه اجباری سرویس‌های بیرونی صفر باشد یا صریحاً به‌عنوان مانع MVP اعلام شود.
- سازگاری Windows 7 / Firefox 115 ESR دارای ماتریس، محدودیت و روش آزمون باشد.
- محاسبات و تاریخ‌های نمونه با تست مشخص شده باشند.
- هیچ کد برنامه‌ای تغییر نکرده باشد.
- کل کار در branch و commitهای محلی قابل ادامه باشد.
- مدیر پروژه/عامل چهارم پیش از تأیید مالک، مجوز پیاده‌سازی صادر نکند.

## 7. Prompt کوتاه برای شروع

Use Codex with my existing ChatGPT Free account and work only on the local Git repository. Do not use Codex Cloud, API keys, billing, credits or paid services. Read this Gate and the RFP v0.3. First inspect the repository and prepare the architecture proposal only. Do not code. If usage limits are reached, stop and leave all progress in Git commits. Never ask me to upgrade.
