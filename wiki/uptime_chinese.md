# [Linux] Bash uptime 使用说明: 显示系统运行时间和负载

## 概述
`uptime` 命令用于显示系统自上次启动以来的运行时间，以及当前系统的负载情况。它提供了系统的运行状态，帮助用户了解系统的性能和负载情况。

## 用法
基本语法如下：
```
uptime [options]
```

## 常用选项
- `-p`：以人类可读的格式显示系统的运行时间。
- `-s`：显示系统的启动时间。
- `-h`：显示帮助信息。

## 常见示例
1. 显示系统的运行时间和负载：
   ```bash
   uptime
   ```

2. 以人类可读的格式显示运行时间：
   ```bash
   uptime -p
   ```

3. 显示系统的启动时间：
   ```bash
   uptime -s
   ```

## 提示
- 定期检查系统的运行时间和负载，可以帮助你及时发现性能瓶颈。
- 在进行系统维护或更新之前，使用 `uptime` 命令确认系统的负载情况，以避免在高负载时进行操作。