# Create Chronicles: Bosses and Beyond — фикс для хоста

Пакет для **хоста** (LAN-сервера) и второго игрока. Сборка **2.5.3**, Minecraft **1.20.1**, Forge **47.3.0**.

## Что внутри

| Папка | Назначение |
|-------|------------|
| `kubejs/` | Скрипты, рецепты, текстуры (658 файлов) — **обязательно** |
| `defaultconfigs/` | Серверные конфиги модов |
| `quests-ru/` | **Все квесты на русском** (31 глава) |

Без `kubejs` не работают кастомные предметы (`rotation_mechanism`, машины, очки навыков и т.д.).

## Быстрая установка

Подробная инструкция: **[INSTALL-HOST.md](INSTALL-HOST.md)**

1. Бэкап мира → `saves\ИмяМира_backup`
2. Закрыть Minecraft
3. Скопировать в `%appdata%\.minecraft\`:
   - `kubejs/` → `kubejs/`
   - `defaultconfigs/` → `defaultconfigs/`
   - `quests-ru/config/ftbquests/quests/` → `config/ftbquests/quests/`
4. Полный перезапуск игры

## Проверка

- JEI: **Rotation Mechanism** находится
- Квесты: текст на русском
- Лог: `logs/kubejs/startup.log` — `launch.js`, `main.js` (не только `example.js`)

## Cursor на ПК хоста

Промпт для автоматической установки: **[PROMPT-DLYA-CURSOR.md](PROMPT-DLYA-CURSOR.md)**

## Ссылки

- Репозиторий: https://github.com/MatveiShadchin/create-chronicles-host-fix
- Сборка: https://www.curseforge.com/minecraft/modpacks/create-chronicles-bosses-and-beyond
