# [لينكس] Bash ulimit: تحديد موارد النظام

## Overview
يستخدم أمر `ulimit` في Bash لتحديد حدود موارد النظام التي يمكن أن تستخدمها العمليات الجارية. يساعد هذا الأمر في إدارة استخدام الذاكرة، وعدد العمليات، وغيرها من الموارد، مما يساهم في تحسين أداء النظام ومنع استهلاك الموارد بشكل مفرط.

## Usage
يمكن استخدام الأمر `ulimit` مع خيارات مختلفة لتحديد الحدود المطلوبة. الصيغة الأساسية هي:

```bash
ulimit [options] [arguments]
```

## Common Options
- `-a`: عرض جميع الحدود الحالية.
- `-c`: تحديد الحد الأقصى لحجم ملفات التفريغ (core files).
- `-d`: تحديد الحد الأقصى لحجم الذاكرة الافتراضية.
- `-f`: تحديد الحد الأقصى لحجم الملفات التي يمكن إنشاؤها.
- `-l`: تحديد الحد الأقصى لحجم الذاكرة القابلة للقفل.
- `-m`: تحديد الحد الأقصى لحجم الذاكرة المادية.
- `-n`: تحديد الحد الأقصى لعدد الملفات المفتوحة.
- `-s`: تحديد الحد الأقصى لحجم مكدس الذاكرة.

## Common Examples
- لعرض جميع الحدود الحالية:
```bash
ulimit -a
```

- لتحديد الحد الأقصى لعدد الملفات المفتوحة إلى 1024:
```bash
ulimit -n 1024
```

- لتحديد الحد الأقصى لحجم ملفات التفريغ إلى 0 (تعطيل التفريغ):
```bash
ulimit -c 0
```

- لتحديد الحد الأقصى لحجم الذاكرة الافتراضية إلى 1 جيجابايت:
```bash
ulimit -v 1048576
```

## Tips
- تأكد من أن لديك الأذونات اللازمة لتغيير الحدود، حيث قد تتطلب بعض التغييرات حقوق المستخدم الجذر.
- استخدم `ulimit -a` بشكل دوري لمراقبة الحدود الحالية وتجنب المشاكل المحتملة.
- قم بتعديل الحدود بحذر، حيث يمكن أن تؤثر التغييرات على أداء النظام بشكل عام.