# [لینوکس] Bash uuidgen استفاده: تولید UUID ها

## Overview
دستور `uuidgen` برای تولید شناسه‌های یکتا جهانی (UUID) استفاده می‌شود. این شناسه‌ها معمولاً برای شناسایی یکتا در پایگاه‌های داده، سیستم‌های توزیع‌شده و سایر کاربردهای نرم‌افزاری به کار می‌روند.

## Usage
سینتکس پایه دستور به صورت زیر است:

```bash
uuidgen [options] [arguments]
```

## Common Options
- `-r`: تولید UUID تصادفی.
- `-t`: تولید UUID زمان‌محور.
- `-h`: نمایش راهنما و اطلاعات مربوط به استفاده از دستور.

## Common Examples
در اینجا چند مثال عملی از استفاده از دستور `uuidgen` آورده شده است:

### تولید یک UUID تصادفی
```bash
uuidgen
```

### تولید چند UUID
```bash
uuidgen -n 5
```

### تولید UUID زمان‌محور
```bash
uuidgen -t
```

### تولید UUID تصادفی با خروجی به فایل
```bash
uuidgen > my_uuid.txt
```

## Tips
- برای تولید چند UUID به صورت همزمان، می‌توانید از حلقه‌های Bash استفاده کنید.
- UUID ها به طور کلی ۳۲ کاراکتر طول دارند و می‌توانند به راحتی در پایگاه‌های داده ذخیره شوند.
- همیشه از UUID ها در سیستم‌های توزیع‌شده استفاده کنید تا از تداخل شناسه‌ها جلوگیری شود.