# [Linux] Bash fg การใช้งาน: ใช้เพื่อนำงานที่อยู่เบื้องหลังกลับมาทำงานในพื้นหลัง

## Overview
คำสั่ง `fg` ใช้เพื่อนำงานที่ถูกหยุดหรือทำงานในพื้นหลังกลับมาทำงานในพื้นหลัง โดยจะทำให้ผู้ใช้สามารถควบคุมงานนั้นได้อีกครั้งในเทอร์มินัล

## Usage
รูปแบบพื้นฐานของคำสั่ง `fg` คือ:

```bash
fg [options] [job_spec]
```

## Common Options
- `job_spec`: ระบุหมายเลขหรือชื่อของงานที่ต้องการนำกลับมาทำงาน
- `-n`: ใช้เพื่อระบุให้ทำงานกับงานล่าสุดที่ถูกหยุด
- `-p`: ใช้เพื่อระบุหมายเลขของโปรเซสที่ต้องการนำกลับมา

## Common Examples
1. นำงานล่าสุดที่ถูกหยุดกลับมาทำงาน:
   ```bash
   fg
   ```

2. นำงานที่มีหมายเลข 1 กลับมาทำงาน:
   ```bash
   fg %1
   ```

3. นำงานที่มีชื่อ "myjob" กลับมาทำงาน:
   ```bash
   fg %myjob
   ```

4. นำงานล่าสุดที่ถูกหยุดกลับมาทำงานโดยไม่ระบุหมายเลข:
   ```bash
   fg -n
   ```

## Tips
- หากคุณไม่แน่ใจว่างานใดอยู่ในสถานะเบื้องหลัง สามารถใช้คำสั่ง `jobs` เพื่อดูรายการงานทั้งหมดได้
- คำสั่ง `fg` จะทำให้คุณสามารถกลับไปทำงานที่ถูกหยุดได้อย่างรวดเร็ว โดยไม่ต้องเริ่มใหม่ทั้งหมด
- หากต้องการหยุดงานที่ทำอยู่ในพื้นหลัง สามารถใช้ `Ctrl + Z` เพื่อหยุดงานนั้นก่อนที่จะใช้ `fg` นำกลับมา