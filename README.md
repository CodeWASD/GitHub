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
