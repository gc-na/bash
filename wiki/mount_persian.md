# [لینوکس] Bash mount استفاده: [نصب سیستم فایل]

## Overview
دستور `mount` در لینوکس برای متصل کردن سیستم‌های فایل به دایرکتوری‌های موجود در سیستم استفاده می‌شود. این دستور به شما امکان می‌دهد تا دیسک‌ها و پارتیشن‌ها را به سیستم خود اضافه کنید و به داده‌های موجود در آن‌ها دسترسی پیدا کنید.

## Usage
سینتکس پایه دستور `mount` به صورت زیر است:

```
mount [options] [arguments]
```

## Common Options
- `-t` : نوع سیستم فایل را مشخص می‌کند.
- `-o` : گزینه‌های اضافی برای نصب سیستم فایل را تعیین می‌کند.
- `-a` : همه سیستم‌های فایل مشخص شده در `/etc/fstab` را نصب می‌کند.
- `-r` : سیستم فایل را به صورت فقط خواندنی نصب می‌کند.

## Common Examples
در اینجا چند مثال عملی از استفاده از دستور `mount` آورده شده است:

1. نصب یک پارتیشن خاص:
   ```bash
   mount /dev/sda1 /mnt
   ```

2. نصب یک سیستم فایل با مشخص کردن نوع آن:
   ```bash
   mount -t ext4 /dev/sda1 /mnt
   ```

3. نصب همه سیستم‌های فایل مشخص شده در `/etc/fstab`:
   ```bash
   mount -a
   ```

4. نصب یک سیستم فایل به صورت فقط خواندنی:
   ```bash
   mount -o ro /dev/sda1 /mnt
   ```

## Tips
- قبل از نصب یک سیستم فایل، مطمئن شوید که دایرکتوری مقصد وجود دارد.
- برای مشاهده سیستم‌های فایل نصب شده، می‌توانید از دستور `df -h` استفاده کنید.
- همیشه پس از اتمام کار با سیستم فایل، از دستور `umount` برای جدا کردن آن استفاده کنید تا از آسیب به داده‌ها جلوگیری شود.