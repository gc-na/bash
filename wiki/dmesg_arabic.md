# [لينكس] Bash dmesg الاستخدام: عرض رسائل النواة

## نظرة عامة
أمر `dmesg` يُستخدم لعرض رسائل النواة في نظام التشغيل، والتي تتضمن معلومات حول الأجهزة، والأخطاء، والأحداث التي تحدث أثناء تشغيل النظام. هذه الرسائل تُعتبر مفيدة لتشخيص المشاكل وفهم سلوك النظام.

## الاستخدام
التركيب الأساسي للأمر هو:

```bash
dmesg [خيارات] [وسائط]
```

## الخيارات الشائعة
- `-C` : مسح سجل رسائل النواة.
- `-c` : عرض الرسائل ثم مسح السجل.
- `-n LEVEL` : تعيين مستوى الرسائل المراد عرضها.
- `-T` : عرض الطوابع الزمنية للرسائل بشكل مقروء.
- `--help` : عرض معلومات المساعدة حول الأمر.

## أمثلة شائعة
- لعرض جميع رسائل النواة:
  ```bash
  dmesg
  ```

- لعرض الرسائل مع الطوابع الزمنية:
  ```bash
  dmesg -T
  ```

- لمسح سجل رسائل النواة بعد عرضها:
  ```bash
  dmesg -c
  ```

- لتعيين مستوى الرسائل المعروضة إلى 3 (تحذيرات):
  ```bash
  dmesg -n 3
  ```

## نصائح
- استخدم `dmesg -T` لفهم الرسائل بشكل أفضل، حيث يعرض الطوابع الزمنية بشكل مقروء.
- تأكد من مراجعة الرسائل بعد تثبيت أجهزة جديدة أو تحديث النظام، حيث يمكن أن تكشف عن مشاكل محتملة.
- يمكنك دمج `dmesg` مع أدوات أخرى مثل `grep` لتصفية الرسائل، على سبيل المثال:
  ```bash
  dmesg | grep error
  ```