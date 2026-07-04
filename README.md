# Create Chronicles — фикс для хоста и русские квесты

Репозиторий для **LAN-хоста** и второго игрока. Сборка **2.5.3**, Minecraft **1.20.1**.

## Что тебе нужно?

| Задача | Инструкция |
|--------|------------|
| **Только русские квесты** | **[INSTALL-QUESTS-RU.md](INSTALL-QUESTS-RU.md)** ← для хоста, если kubejs уже есть |
| Полный фикс (предметы + квесты) | [INSTALL-HOST.md](INSTALL-HOST.md) |

## Только перевод (кратко)

Скопируй `quests-ru/config/ftbquests/quests/` → `.minecraft/config/ftbquests/quests/`

ZIP: https://github.com/MatveiShadchin/create-chronicles-host-fix/archive/refs/heads/main.zip

## Полный пакет

| Папка | Назначение |
|-------|------------|
| `quests-ru/` | Все квесты на русском (31 глава) |
| `kubejs/` | Предметы и рецепты сборки (если не работает JEI) |
| `defaultconfigs/` | Конфиги модов (опционально) |

## Проверка

- JEI: **Rotation Mechanism** находится
- Квесты: текст на русском
- Лог: `logs/kubejs/startup.log` — `launch.js`, `main.js` (не только `example.js`)

## Cursor на ПК хоста

Промпт для автоматической установки: **[PROMPT-DLYA-CURSOR.md](PROMPT-DLYA-CURSOR.md)**

## Ссылки

- Репозиторий: https://github.com/MatveiShadchin/create-chronicles-host-fix
- Сборка: https://www.curseforge.com/minecraft/modpacks/create-chronicles-bosses-and-beyond
