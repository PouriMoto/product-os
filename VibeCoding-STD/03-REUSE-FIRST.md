# 03 — Reuse First

طبق قانون ۱ در `01-CONSTITUTION.md`، قبل از نوشتن هر ماژول زیرساختی، باید گزینه‌های آماده بررسی شوند.
این فایل نقطه شروع آن بررسی است — لیست کامل و همیشه‌به‌روز نیست، اما یادآوری می‌کند که کجا نباید از صفر کد نوشت.

هر بار قبل از استفاده، وضعیت گزینه‌ها را با یک جست‌وجوی سریع تأیید کن؛ این حوزه سریع تغییر می‌کند.

---

| نیاز | اول این را بررسی کن | چه زمانی خودت بسازی |
|---|---|---|
| Authentication | Supabase Auth، Clerk، Auth0، Firebase Auth، Better Auth | فقط اگر نیاز به منطق سفارشی خیلی خاص باشد که هیچ‌کدام پشتیبانی نمی‌کند |
| Authorization / RBAC | امکانات داخلی فریم‌ورک، CASL، Permit.io | فقط اگر مدل دسترسی خیلی غیرمعمول است |
| Storage / Upload فایل | S3، Cloudinary، Supabase Storage | تقریباً هیچ‌وقت لازم نیست خودت بنویسی |
| Billing / Subscription | Stripe، Paddle، LemonSqueezy | فقط منطق تجاری خاص روی بالای آن‌ها |
| Database / ORM | Supabase، PostgreSQL + Prisma/Drizzle | — |
| Analytics محصول | PostHog، Plausible، Mixpanel | فقط اگر Analytics خودِ محصول است (مزیت رقابتی) |
| Notification (Email/SMS) | Resend، SendGrid، Kavenegar (برای ایران) | تقریباً هیچ‌وقت |
| QR / Barcode | کتابخانه‌های استاندارد موجود (qrcode.js و مشابه) | تقریباً هیچ‌وقت |
| Error Tracking | Sentry | — |
| Logging / Monitoring | Better Stack، Datadog، خدمات هاست (Liara/Arvan) | فقط تنظیمات سفارشی روی این‌ها |
| CI/CD | GitHub Actions، پلتفرم هاست | — |
| Date/Time handling | یک کتابخانه ثابت انتخاب کن (مثل date-fns) و همان‌جا بمان | هیچ‌وقت خودت الگوریتم تاریخ ننویس |

---

## چیزی که همیشه خودت می‌سازی (مزیت رقابتی)

این‌ها استثنای قانون Reuse First‌اند، چون هویت محصول تو هستند:

- منطق اختصاصی AI / Agent مربوط به محصول به جز وقتی که از n8n استفاده میکنی (هنگام استفاده از n8n بپرس آیا community nodes آماده هست یا فایل workflow.json آماده یا مسابه وجود دارد؟
- Workflow اختصاصی کسب‌وکار
- ساختار داده و منطق خاص محصول (مثل Customer Vault، بازی سفارشی)
- رابط کاربری و تجربه کاربری

## الگوی بررسی سریع (پیش از هر Feature)

1. نیاز را در یک جمله بنویس.
2. یک جست‌وجوی سریع بزن: `"[نیاز] service OR library 2026"`.
3. اگر گزینه معتبر و پرکاربرد پیدا شد → استفاده کن، فقط تنظیمش کن.
4. اگر نه → طبق قانون ۱ Constitution، فقط در این حالت کد جدید بنویس.
