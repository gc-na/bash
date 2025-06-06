# [Linux] Bash reboot 用法: 重新啟動系統

## Overview
`reboot` 命令用於重新啟動系統。當執行此命令時，系統會關閉所有運行中的進程，然後重新啟動。這在需要應用更新或修復系統問題時非常有用。

## Usage
基本語法如下：
```
reboot [options] [arguments]
```

## Common Options
- `-f`：強制重新啟動，跳過正常關閉程序的過程。
- `-p`：關閉電源，而不僅僅是重新啟動。
- `-n`：不進行同步，直接重新啟動。

## Common Examples
1. **正常重新啟動系統**：
   ```bash
   reboot
   ```

2. **強制重新啟動系統**：
   ```bash
   reboot -f
   ```

3. **關閉電源而不重新啟動**：
   ```bash
   reboot -p
   ```

4. **不進行同步直接重新啟動**：
   ```bash
   reboot -n
   ```

## Tips
- 在使用 `reboot` 命令之前，確保已保存所有未保存的工作，以免資料遺失。
- 使用 `-f` 選項時要小心，因為這會強制關閉所有進程，可能導致資料損壞。
- 如果系統無法正常關閉，考慮使用 `-n` 選項來跳過同步，但這可能會帶來風險。