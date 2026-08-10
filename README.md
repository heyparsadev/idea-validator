# idea-validator

**اعتبارسنجی ایدهٔ استارتاپی برای Claude Code** — پیاده‌سازی فصل ۳ کتاب *The Founder's Playbook: Building an AI-Native Startup* (Anthropic, 2026).

An Idea-stage validation plugin for Claude Code, implementing Chapter 3 of Anthropic's *The Founder's Playbook*.

---

## چرا / Why

کدنویسی agentic فاصلهٔ بین «یه ایده دارم» و «یه محصول دارم» رو تقریباً صفر کرده. ۴۲٪ استارتاپ‌ها شکست خوردن چون چیزی ساختن که کسی نمی‌خواست — **قبل** از اینکه ساختن انقدر ارزون بشه.

مشکل دوم ظریف‌تره: AI هر چیزی که ازش بخوای رو برات پیدا می‌کنه. ازش بخواه ایده‌ات رو تأیید کنه، شواهد تأییدی می‌آره. ازش بخواه بازارت رو سایز کنه، عددی می‌آره که TAM‌ات قابل‌سرمایه‌گذاری به‌نظر برسه. یعنی حالا می‌شه **سریع‌تر از همیشه یه پروندهٔ مفصل و خوش‌ظاهر برای یه ایدهٔ بد ساخت** — در حالی که کاملاً مطمئنی داری due diligence می‌کنی.

این پلاگین برای اینه که sense-making جلوتر از building بمونه.

> Agentic coding collapsed the distance between "I have an idea" and "I have a product," and AI research gave confirmation bias an engine. This plugin exists to keep sense-making ahead of building.

---

## نصب / Install

از داخل Claude Code / From inside Claude Code:

```
/plugin marketplace add https://github.com/heyparsadev/claude-plugins.git
/plugin install founder-playbook@parsa-plugins
```

یا با CLI / Or via the CLI:

```bash
claude plugin marketplace add https://github.com/heyparsadev/claude-plugins.git
claude plugin install founder-playbook@parsa-plugins
```

مارکت‌پلیس [claude-plugins](https://github.com/heyparsadev/claude-plugins) پلاگین‌های دیگر را هم دارد. اگر فقط همین یکی را می‌خواهی، از این ریپو مستقیم هم نصب می‌شود:

The [claude-plugins](https://github.com/heyparsadev/claude-plugins) marketplace carries the other plugins too. To install this one alone, use this repo directly:

```
/plugin marketplace add https://github.com/heyparsadev/idea-validator.git
/plugin install founder-playbook@idea-validator
```

> 💡 از URL کامل `https://...git` استفاده کن (نه `owner/repo`) تا clone از HTTPS انجام شه و به SSH key نیاز نباشه.
> Use the full `https://...git` URL so cloning uses HTTPS and needs no SSH key.

بعد یک سشن جدید Claude Code باز کن — پلاگین‌ها اول سشن لود می‌شن.
Then start a new Claude Code session; plugins load at session start.

---

## شروع / Usage

```
/founder-playbook:idea  ایده‌ات رو اینجا بنویس
```

همین. بقیه میان‌برن:

```
/founder-playbook:stage-map        ← اصلاً تو کدوم مرحله‌ای؟
/founder-playbook:idea-redteam     ← فقط پاس تهاجمی روی یک فرضیه
/founder-playbook:idea-gate        ← فقط امتیازدهی گیت خروج
```

یا فقط طبیعی حرف بزن — «این ایده ارزش ساختن داره؟» یا «فرضیه‌ام رو تست کن» — اسکیل خودش فعال می‌شه. فارسی و انگلیسی هر دو.

Or just talk naturally — "is this worth building?", "poke holes in this idea" — the skill auto-activates. Works in Persian and English.

---

## سه حالت / Three modes

| حالت | چی می‌شه |
|---|---|
| **Coach** | یه سؤال تیز در لحظه، خودت فکر می‌کنی، Claude چالش می‌کنه و می‌نویسه. کندتره، ولی آخرش واقعاً بازارت رو می‌شناسی. |
| **Auto** | Claude مراحل ۱–۶ و ۸–۱۰ رو خودش end-to-end اجرا می‌کنه و کل داسیه رو تحویل می‌ده، با علامت‌گذاری هر فرض. |
| **Hybrid** ⭐ | Auto برای مراحل تحقیقی، Coach برای مراحل قضاوتی. پیش‌فرض پیشنهادی. |

### دیوار مرحلهٔ ۷

**حالت auto نمی‌تونه problem-solution fit تولید کنه** — و این رو از اول اعلام می‌کنه، نه آخر کار.

اون یه فرضیهٔ تیز و آبدیده، یه red team جدی، نقشهٔ رقبا، مدل بازار، و یه پلن مصاحبهٔ آمادهٔ اجرا تحویل می‌ده. همه‌شون کار دسکی‌ان. **مصاحبهٔ واقعی با آدم واقعی تنها منبع شواهد درجه A است** و هیچ مدلی نمی‌تونه جای فاندر انجامش بده.

چیزی که auto سر این دیوار می‌تونه بکنه: لیست پروسپکت، دراف outreach، کدنس پیگیری، شیت ترکینگ، و تمرین مصاحبه با پرسونای `[SIMULATED]` (که همیشه درجه D می‌گیره و هیچ‌وقت از گیت رد نمی‌شه).

> **Auto mode cannot produce problem–solution fit** — and it says so up front. Step 7 is a wall no mode crosses.

---

## چیزی که گیت رو معنادار می‌کنه / The evidence ledger

هر ادعایی که وارد workspace می‌شه بر اساس **منشأش** نمره می‌گیره:

| نمره | منبع |
|---|---|
| **A** | آدم واقعیِ نام‌برده از پروفایل هدف، تو مصاحبه‌ای که خود فاندر داشته |
| **B** | کاربر واقعی، در فضای عمومی — ریویو، فروم، کامنت اپ‌استور |
| **C** | تحقیق شخص ثالث — گزارش تحلیلگر، نظرسنجی، فایلینگ، ژورنالیسم معتبر |
| **D** | استدلال مدل، تخمین، یا خروجی `[SIMULATED]` |

**هیچ شرط خروجی با شواهد درجه D تنها پاس نمی‌شه.** «آیا مسئله واقعی و مشخصه؟» حتماً A می‌خواد.

وقتی دفتر شواهد چیزی بالاتر از C نداره، گزارش صادقانه اینه: *«تحقیق دسکی تموم شد و فرضیه ازش جون سالم به‌در برد؛ problem-solution fit اثبات نشده و تا مصاحبه‌ها انجام نشه نمی‌شه.»*

بعلاوه:
- **kill criteria قبل از شروع تحقیق** نوشته می‌شه، نه بعدش
- **case مخالف قبل از case موافق** نوشته می‌شه
- **bias audit** بعد از هر سنتز — ۶ سؤال، جواب کتبی
- **پروتوتایپ ابزار گفتگوئه، شواهد نیست** — قانون سفت

---

## پایپلاین / The pipeline

| # | مرحله | گیت عبور |
|---|---|---|
| 0 | بریف و kill criteria | فاندر نوشته چی باعث می‌شه بی‌خیال شه |
| 1 | ساخت فرضیهٔ آزمون‌پذیر | از rubric چهارسؤالی رد شه |
| 2 | Red team | حداقل یک یافته که واقعاً نگرانش کنه |
| 3 | نقشهٔ رقبا (۴ لایه) | استدلال «چرا اونا برنده می‌شن و تو نه» قانع‌کننده باشه |
| 4 | بازار + استخراج شکایات | فرض‌های سایزینگ لیست و نقد شده باشن |
| 5 | خوانش ترند | ۳ ترند، هرکدوم tailwind یا headwind مشخص |
| 6 | طراحی مصاحبه | هر سؤال از audit چهارپرچمی رد شه |
| 7 | **اجرای مصاحبه‌ها** | ≥۸ گفتگوی واقعی + سنتز هر ۵ تا |
| 8 | کانسپت راه‌حل | ۳ فرض حیاتی با پیامد شکست هرکدوم |
| 9 | بریف پروتوتایپ | دقیقاً یک تعامل اصلی |
| 10 | گیت خروج | حکم با نمرهٔ شواهد ثبت شه |

**حکم نهایی:** `PROCEED` · `ITERATE` · `PIVOT` · `KILL` · `BLOCKED`

---

## خروجی / Workspace

```
ventures/<slug>/00-idea-stage/
├── STATE.md          ← پیشرفت — بین سشن‌ها ادامه می‌ده، از اول شروع نمی‌کنه
├── EVIDENCE.md       ← دفتر شواهد: هر ادعا، منبع، نمره
├── 00-brief.md … 10-prototype.md
├── 07-interviews/
└── DECISION.md       ← گیت خروج + حکم + لاگ تصمیم
```

با پلاگین [venture](https://github.com/heyparsadev/claude-plugins/tree/main/venture) interop داره: اگه `ventures/<slug>/VENTURE.md` موجود باشه ازش استفاده می‌کنه، وگرنه یه نسخهٔ مینیمال می‌سازه. پوشه‌ها جدان، پس تداخلی نیست.

---

## محتوا / What's inside

**اسکیل‌ها:**
- `idea-stage` — پایپلاین کامل فصل ۳ (۶ فایل reference)
- `stage-map` — نقشهٔ کل کتاب: تشخیص مرحلهٔ فعلی از روی شواهد، goal و exit criteria و failure modes هر چهار مرحله

**ایجنت:** `idea-red-team` — پرامپت شده که **رد کنه**، نه ارزیابی. قوی‌ترین استدلال علیه ایده، شواهد نقض‌کننده، و قبرستان تلاش‌های قبلی با علت مرگ.

**کامندها:** `/idea` · `/idea-redteam` · `/idea-gate`

فصل ۳ عمیق پیاده شده. فصل‌های ۴–۶ (MVP، Launch، Scale) در سطح نقشه توسط `stage-map` پوشش داده شدن و طوری ساختاربندی شدن که بعداً هرکدوم اسکیل مستقل بشن.

---

## License

MIT — see [LICENSE](LICENSE).

بر اساس *The Founder's Playbook: Building an AI-Native Startup*، منتشرشده توسط Anthropic. این پلاگین یک ابزار مستقل است و توسط Anthropic تأیید نشده.

Based on *The Founder's Playbook: Building an AI-Native Startup*, published by Anthropic. This plugin is an independent tool and is not endorsed by Anthropic.
