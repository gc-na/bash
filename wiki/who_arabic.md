# [لينكس] Bash who الاستخدام: عرض معلومات المستخدمين المتصلين

## Overview
يستخدم الأمر `who` في نظام التشغيل لينكس لعرض معلومات حول المستخدمين المتصلين بالنظام. يقوم بإظهار أسماء المستخدمين، وقت تسجيل الدخول، وأحيانًا معلومات إضافية مثل الجهاز الذي تم تسجيل الدخول منه.

## Usage
يمكن استخدام الأمر `who` بالشكل التالي:

```bash
who [options] [arguments]
```

## Common Options
- `-a`: يعرض جميع المعلومات المتاحة عن المستخدمين المتصلين.
- `-b`: يعرض وقت آخر إعادة تشغيل للنظام.
- `-q`: يعرض أسماء المستخدمين المتصلين فقط وعددهم.
- `--help`: يعرض معلومات المساعدة حول الأمر.

## Common Examples
- لعرض جميع المستخدمين المتصلين:
  ```bash
  who
  ```

- لعرض جميع المعلومات المتاحة:
  ```bash
  who -a
  ```

- لعرض وقت آخر إعادة تشغيل للنظام:
  ```bash
  who -b
  ```

- لعرض أسماء المستخدمين المتصلين وعددهم:
  ```bash
  who -q
  ```

## Tips
- يمكنك استخدام الأمر `who` مع الأمر `grep` لتصفية النتائج حسب اسم مستخدم معين.
- تأكد من تشغيل الأمر في بيئة طرفية تدعم عرض المعلومات بشكل صحيح.
- استخدم الخيار `-H` لإضافة رؤوس للأعمدة عند عرض المعلومات، مما يسهل قراءة النتائج.