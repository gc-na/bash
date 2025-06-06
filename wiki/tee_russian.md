# [Linux] Bash tee Использование: Запись вывода в файл и на экран

## Обзор
Команда `tee` в Bash используется для чтения стандартного ввода и записи его одновременно в стандартный вывод и один или несколько файлов. Это позволяет вам видеть вывод команды на экране, а также сохранять его в файл для дальнейшего использования.

## Использование
Основной синтаксис команды `tee` выглядит следующим образом:

```bash
tee [опции] [аргументы]
```

## Общие опции
- `-a`, `--append`: Добавляет вывод в конец файла вместо перезаписи.
- `-i`, `--ignore-interrupts`: Игнорирует прерывания.
- `--help`: Показывает справочную информацию о команде.
- `--version`: Показывает версию команды.

## Общие примеры
Вот несколько практических примеров использования команды `tee`:

1. Запись вывода команды в файл:
   ```bash
   echo "Hello, World!" | tee output.txt
   ```

2. Запись вывода команды в файл с добавлением:
   ```bash
   echo "Another line" | tee -a output.txt
   ```

3. Использование `tee` с несколькими файлами:
   ```bash
   echo "Logging output" | tee file1.txt file2.txt
   ```

4. Запись вывода команды в файл и отображение на экране:
   ```bash
   ls -l | tee directory_list.txt
   ```

## Советы
- Используйте опцию `-a`, если хотите добавлять данные в существующий файл, а не перезаписывать его.
- Команда `tee` полезна для отладки, так как позволяет видеть вывод команды и одновременно сохранять его.
- Если вы хотите записать вывод нескольких команд, можете использовать группировку команд с помощью фигурных скобок:
  ```bash
  { echo "First line"; echo "Second line"; } | tee output.txt
  ```