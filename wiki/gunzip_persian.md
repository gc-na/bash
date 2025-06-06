# [لینوکس] Bash gunzip استفاده: فشرده‌سازی و استخراج فایل‌های gzip

## Overview
دستور `gunzip` برای استخراج فایل‌های فشرده شده با فرمت gzip استفاده می‌شود. این دستور به شما اجازه می‌دهد تا فایل‌های فشرده را به حالت اصلی خود بازگردانید.

## Usage
سینتکس پایه دستور `gunzip` به شکل زیر است:

```bash
gunzip [options] [arguments]
```

## Common Options
- `-c`: خروجی را به استاندارد خروجی (stdout) ارسال می‌کند و فایل اصلی را تغییر نمی‌دهد.
- `-f`: فایل‌های موجود را بدون پرسش قبلی بازنویسی می‌کند.
- `-k`: فایل‌های فشرده را حفظ می‌کند و فقط نسخه‌ی استخراج شده را ایجاد می‌کند.
- `-r`: به صورت بازگشتی در دایرکتوری‌ها عمل می‌کند.

## Common Examples
در اینجا چند مثال عملی از استفاده از `gunzip` آورده شده است:

### استخراج یک فایل gzip
برای استخراج یک فایل فشرده به نام `example.gz`:

```bash
gunzip example.gz
```

### استخراج و حفظ فایل اصلی
اگر می‌خواهید فایل اصلی را حفظ کنید و فقط نسخه‌ی استخراج شده را داشته باشید:

```bash
gunzip -k example.gz
```

### استخراج چندین فایل
برای استخراج چندین فایل gzip به طور همزمان:

```bash
gunzip file1.gz file2.gz file3.gz
```

### استخراج فایل و ارسال به stdout
برای مشاهده محتوای فایل فشرده بدون ذخیره آن:

```bash
gunzip -c example.gz
```

## Tips
- همیشه قبل از استفاده از `gunzip` از فایل‌های مهم خود نسخه پشتیبان تهیه کنید.
- از گزینه `-k` استفاده کنید تا از حذف ناخواسته فایل‌های فشرده جلوگیری کنید.
- برای کار با دایرکتوری‌های بزرگ، از گزینه `-r` استفاده کنید تا به راحتی تمام فایل‌های gzip را استخراج کنید.