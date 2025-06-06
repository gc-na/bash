# [لینوکس] Bash ping استفاده: بررسی دسترسی به شبکه

## Overview
دستورات `ping` برای بررسی دسترسی و وضعیت ارتباط بین دو دستگاه در شبکه استفاده می‌شود. این دستور بسته‌های داده‌ای به یک آدرس IP یا نام دامنه ارسال می‌کند و زمان پاسخ را اندازه‌گیری می‌کند.

## Usage
سینتکس پایه دستور `ping` به صورت زیر است:

```bash
ping [options] [arguments]
```

## Common Options
- `-c [number]`: تعداد بسته‌هایی که باید ارسال شوند را مشخص می‌کند.
- `-i [seconds]`: زمان بین ارسال بسته‌ها را به ثانیه تنظیم می‌کند.
- `-s [size]`: اندازه بسته‌های داده‌ای را مشخص می‌کند.
- `-t [ttl]`: مقدار TTL (Time to Live) را تنظیم می‌کند.

## Common Examples
- **پینگ یک آدرس IP:**
```bash
ping 8.8.8.8
```

- **پینگ یک دامنه:**
```bash
ping google.com
```

- **ارسال 5 بسته:**
```bash
ping -c 5 google.com
```

- **تنظیم زمان بین بسته‌ها به 2 ثانیه:**
```bash
ping -i 2 google.com
```

## Tips
- برای بررسی اتصال به اینترنت، می‌توانید از آدرس IP عمومی مانند `8.8.8.8` استفاده کنید.
- اگر می‌خواهید فقط زمان پاسخ را بررسی کنید، می‌توانید از گزینه `-c` برای محدود کردن تعداد بسته‌ها استفاده کنید.
- در صورتی که با مشکلات اتصال مواجه شدید، از گزینه‌های مختلف برای عیب‌یابی استفاده کنید، مانند تغییر TTL یا اندازه بسته.