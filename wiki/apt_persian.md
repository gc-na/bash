# [لینوکس] Bash apt استفاده: مدیریت بسته‌ها در سیستم‌های مبتنی بر دبیان

## Overview
دستور `apt` (Advanced Package Tool) ابزاری برای مدیریت بسته‌ها در سیستم‌های مبتنی بر دبیان مانند اوبونتو است. این دستور به کاربران این امکان را می‌دهد که بسته‌های نرم‌افزاری را نصب، حذف و به‌روزرسانی کنند.

## Usage
سینتکس پایه دستور `apt` به صورت زیر است:

```bash
apt [options] [arguments]
```

## Common Options
- `install`: نصب یک یا چند بسته نرم‌افزاری.
- `remove`: حذف یک یا چند بسته نرم‌افزاری.
- `update`: به‌روزرسانی فهرست بسته‌ها.
- `upgrade`: به‌روزرسانی بسته‌های نصب‌شده به آخرین نسخه.
- `search`: جستجوی بسته‌ها بر اساس نام یا توضیحات.

## Common Examples
- نصب یک بسته نرم‌افزاری:
  ```bash
  sudo apt install package_name
  ```

- حذف یک بسته نرم‌افزاری:
  ```bash
  sudo apt remove package_name
  ```

- به‌روزرسانی فهرست بسته‌ها:
  ```bash
  sudo apt update
  ```

- به‌روزرسانی همه بسته‌های نصب‌شده:
  ```bash
  sudo apt upgrade
  ```

- جستجوی یک بسته:
  ```bash
  apt search package_name
  ```

## Tips
- همیشه قبل از نصب یا به‌روزرسانی بسته‌ها، از دستور `apt update` استفاده کنید تا فهرست بسته‌ها به‌روز باشد.
- برای حذف بسته‌ها، از گزینه `--purge` استفاده کنید تا تنظیمات مربوط به بسته نیز حذف شود.
- می‌توانید از `apt list --installed` برای مشاهده لیست بسته‌های نصب‌شده استفاده کنید.