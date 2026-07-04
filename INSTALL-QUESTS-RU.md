# Русские квесты — установка (только перевод)

Если **kubejs уже стоит** и предметы в JEI работают — нужна только эта папка.

## Скачать

**ZIP:** https://github.com/MatveiShadchin/create-chronicles-host-fix/archive/refs/heads/main.zip

Распакуй и найди папку:
```
quests-ru\config\ftbquests\quests\
```

## Промпт для Cursor

Открой **[PROMPT-QUESTS-RU.md](PROMPT-QUESTS-RU.md)** — там готовый текст для вставки в чат Agent.

Кратко:
1. Cursor → Open Folder → `%appdata%\.minecraft`
2. Новый чат → скопировать промпт из PROMPT-QUESTS-RU.md
3. Перезапустить Minecraft

## Установка

1. Закрой Minecraft полностью.
2. Открой `%appdata%\.minecraft\`
3. Скопируй содержимое `quests-ru\config\ftbquests\quests\` в:
   ```
   %appdata%\.minecraft\config\ftbquests\quests\
   ```
   (замени файлы в папке `quests`)

4. Запусти игру и открой мир.

## Проверка

Книга квестов → текст на русском.

Если не обновилось: в чате `/ftbquests reload` или перезапуск мира.

## Одной командой (PowerShell)

```powershell
$mc = "$env:APPDATA\.minecraft"
$zip = "$env:TEMP\cc-quests-ru.zip"
Invoke-WebRequest "https://github.com/MatveiShadchin/create-chronicles-host-fix/archive/refs/heads/main.zip" -OutFile $zip
Expand-Archive $zip "$env:TEMP\cc-quests-ru" -Force
Copy-Item "$env:TEMP\cc-quests-ru\create-chronicles-host-fix-main\quests-ru\config\ftbquests\quests\*" "$mc\config\ftbquests\quests\" -Recurse -Force
Write-Host "Готово! Перезапусти Minecraft."
```

## Что внутри

- 31 глава квестов на русском
- `chapter_groups.snbt` — названия групп
- `data.snbt` — заголовок книги квестов

**Kubejs и defaultconfigs ставить не нужно** — только если не работают предметы вроде Rotation Mechanism (тогда см. INSTALL-HOST.md).
