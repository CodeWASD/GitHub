# GitReleaseLab

## Repository

<div dir="rtl">

به‌صورت پیش‌فرض، <span dir="ltr">Git</span> در یک دایرکتوری تعریف نشده است و فایل‌های آن دایرکتوری را ردیابی نمی‌کند.

اگر به‌صورت محلی (<span dir="ltr">Local</span>) کار می‌کنیم، با استفاده از دستور زیر می‌توانیم یک <span dir="ltr">Repository</span> جدید ایجاد کنیم:

</div>

```bash
git init
```

<div dir="rtl">

با اجرای این دستور، یک پوشه‌ی مخفی به نام `.git` ایجاد می‌شود.

پوشه‌ی `.git` مانند یک پایگاه داده برای <span dir="ltr">Repository</span> عمل می‌کند و اطلاعات مربوط به تاریخچه‌ی <span dir="ltr">Commit</span>ها، <span dir="ltr">Branch</span>ها، تنظیمات <span dir="ltr">Repository</span> و سایر اطلاعات موردنیاز <span dir="ltr">Git</span> را نگهداری می‌کند.

</div>

## Working Tree

<div dir="rtl">

هر <span dir="ltr">Git Repository</span> از چند بخش اصلی تشکیل شده است که <span dir="ltr">Working Tree</span> یکی از آن‌هاست.

<span dir="ltr">Working Tree</span> شامل فایل‌های پروژه در وضعیت فعلی آن‌ها است؛ یعنی فایل‌هایی که در حال حاضر روی آن‌ها کار می‌کنیم و ممکن است تغییراتی در آن‌ها ایجاد شده باشد.

</div>

## Staging Area

<div dir="rtl">

یکی دیگر از بخش‌های مهم <span dir="ltr">Git Repository</span>، بخش <span dir="ltr">Staging Area</span> است.

وقتی روی فایل‌های موجود در <span dir="ltr">Working Tree</span> تغییراتی اعمال می‌کنیم یا فایل جدیدی به پروژه اضافه می‌کنیم، می‌توانیم تغییرات موردنظر را برای ثبت شدن آماده کنیم.

فایل‌ها و تغییراتی که برای <span dir="ltr">commit</span> بعدی انتخاب و آماده شده‌اند، در <span dir="ltr">Staging Area</span> قرار می‌گیرند.

برای اضافه کردن یک فایل به <span dir="ltr">Staging Area</span> می‌توان از دستور زیر استفاده کرد:

</div>

```bash
git add <file-name>
```

<div dir="rtl">

برای اضافه کردن تمام تغییرات می‌توان از دستور زیر استفاده کرد:

</div>

```bash
git add .
```
## Commit / Snapshot

<div dir="rtl">

بعد از اینکه تغییرات فایل‌ها در <span dir="ltr">Staging Area</span> آماده‌ی ثبت شدند، با استفاده از دستور زیر می‌توان آن‌ها را ثبت کرد:

</div>

```bash
git commit -m "commit message"
```

<div dir="rtl">

با اجرای دستور <span dir="ltr">`git commit`</span>، از تغییراتی که در <span dir="ltr">Staging Area</span> قرار دارند یک <span dir="ltr">Snapshot</span> ایجاد می‌شود.

هر <span dir="ltr">Commit</span> در واقع یک نقطه‌ی ثبت‌شده از وضعیت پروژه است که می‌توان بعداً در تاریخچه‌ی <span dir="ltr">Git</span> به آن مراجعه کرد.

نکته: <span dir="ltr">Commit</span> فقط تغییراتی را ثبت می‌کند که قبلاً با دستور <span dir="ltr">`git add`</span> به <span dir="ltr">Staging Area</span> اضافه شده‌اند.

</div>
## Branch

<div dir="rtl">

از آنجایی که <span dir="ltr">Git</span> یک سیستم <span dir="ltr">Version Control</span> است، امکان کار روی چند شاخه یا <span dir="ltr">Branch</span> مختلف را فراهم می‌کند.

استفاده از <span dir="ltr">Branch</span> باعث می‌شود چند توسعه‌دهنده بتوانند هم‌زمان روی بخش‌های مختلف یک پروژه کار کنند. همچنین می‌توان برای توسعه‌ی یک قابلیت جدید، رفع یک مشکل یا آزمایش تغییرات، یک شاخه‌ی جداگانه ایجاد کرد.

شاخه‌ی اصلی پروژه معمولاً <span dir="ltr">`main`</span> یا در برخی پروژه‌های قدیمی‌تر <span dir="ltr">`master`</span> نام دارد.

برای ایجاد یک <span dir="ltr">Branch</span> جدید می‌توان از دستور زیر استفاده کرد:

</div>

```bash
git branch <branch-name>
```

<div dir="rtl">

برای رفتن به <span dir="ltr">Branch</span> موردنظر می‌توان از دستور زیر استفاده کرد:

</div>

```bash
git switch <branch-name>
```

<div dir="rtl">

هر <span dir="ltr">Branch</span> مسیر مستقلی از <span dir="ltr">Commit</span>ها را دنبال می‌کند. بنابراین <span dir="ltr">Commit</span>هایی که روی یک <span dir="ltr">Branch</span> انجام می‌شوند، مستقیماً شاخه‌های دیگر را تغییر نمی‌دهند.

در صورت نیاز، می‌توان تغییرات یک <span dir="ltr">Branch</span> را بعداً با استفاده از عملیاتی مانند <span dir="ltr">`merge`</span> وارد شاخه‌ی دیگری کرد.

</div>

