# [Linux] Bash dmesg 使用法: カーネルメッセージの表示

## Overview
`dmesg` コマンドは、カーネルリングバッファに記録されたメッセージを表示します。主にシステムの起動時やデバイスの状態に関する情報を確認するために使用されます。

## Usage
基本的な構文は次のとおりです。

```
dmesg [options] [arguments]
```

## Common Options
- `-C` : カーネルリングバッファをクリアします。
- `-n level` : メッセージの出力レベルを設定します。
- `-T` : タイムスタンプを人間が読める形式で表示します。
- `-f facility` : 特定のファシリティのメッセージのみを表示します。

## Common Examples
以下は、`dmesg` コマンドの実用的な例です。

### 1. カーネルメッセージの表示
```bash
dmesg
```

### 2. タイムスタンプを人間が読める形式で表示
```bash
dmesg -T
```

### 3. 特定のファシリティのメッセージを表示
```bash
dmesg -f kern
```

### 4. カーネルリングバッファをクリア
```bash
dmesg -C
```

## Tips
- `dmesg` の出力は非常に多くなることがあるため、`less` コマンドと組み合わせてページングすることをお勧めします。
  ```bash
  dmesg | less
  ```
- システムのトラブルシューティングを行う際には、特にデバイスのエラーや警告メッセージに注目してください。
- 定期的に `dmesg` の出力を確認することで、ハードウェアの問題を早期に発見できます。