# [Linux] Bash resize2fs 用法: 调整文件系统大小

## 概述
`resize2fs` 是一个用于调整 ext2、ext3 和 ext4 文件系统大小的命令。它可以在文件系统已挂载的情况下调整其大小，也可以在文件系统未挂载时进行调整。

## 用法
基本语法如下：
```bash
resize2fs [选项] [参数]
```

## 常用选项
- `-f`：强制调整文件系统大小，即使文件系统看起来是健康的。
- `-p`：在调整过程中显示进度信息。
- `-M`：将文件系统缩小到最小大小。
- `-s`：调整文件系统大小以匹配设备大小。

## 常见示例
1. **调整文件系统到最大可用空间**
   ```bash
   resize2fs /dev/sda1
   ```

2. **强制调整文件系统大小**
   ```bash
   resize2fs -f /dev/sda1
   ```

3. **调整文件系统到特定大小**
   ```bash
   resize2fs /dev/sda1 20G
   ```

4. **显示调整进度**
   ```bash
   resize2fs -p /dev/sda1
   ```

## 提示
- 在调整文件系统之前，建议备份重要数据，以防数据丢失。
- 确保在调整文件系统时，尽量避免在文件系统上进行写操作。
- 使用 `df -h` 命令检查文件系统的当前大小和使用情况，以便做出更好的调整决策。