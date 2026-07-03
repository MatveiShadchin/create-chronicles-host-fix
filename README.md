# Create Chronicles: Bosses and Beyond — фикс для хоста

Пакет для **хоста** (сервера в LAN). Сборка **2.5.3**, Minecraft **1.20.1**, Forge **47.3.0**.

Без этих файлов не работают кастомные предметы KubeJS (`rotation_mechanism`, машины, очки навыков и т.д.).

## Что внутри

| Папка | Назначение |
|-------|------------|
| `kubejs/` | Скрипты, рецепты и текстуры сборки (658 файлов) |
| `defaultconfigs/` | Серверные конфиги модов (15 файлов) |

## Установка (хост)

1. **Сделай бэкап мира** — папка `saves\ИмяМира`.
2. Закрой Minecraft полностью.
3. Открой папку Minecraft:
   ```
   %appdata%\.minecraft
   ```
   Если играешь через CurseForge — папка инстанса:
   ```
   ...\Instances\Create Chronicles Bosses and Beyond\minecraft
   ```
4. Скопируй содержимое `kubejs/` → в `.minecraft\kubejs\` (замени папку).
5. Скопируй содержимое `defaultconfigs/` → в `.minecraft\defaultconfigs\` (замени или объедини).
6. Запусти Minecraft заново (не `/reload`).

## Установка (второй игрок)

Тот же `kubejs/` и `defaultconfigs/` — версии у обоих должны совпадать.

## Проверка

После перезапуска в JEI (поиск) должен находиться **Rotation Mechanism**.

Логи KubeJS: `.minecraft\logs\kubejs\startup.log` — должны быть `launch.js`, `main.js`, а не только `example.js`.

## Важно

- Рекомендуется **8 GB RAM** для сборки.
- Forge: **47.3.0** (как в манифесте сборки).
- Официальная страница: [CurseForge](https://www.curseforge.com/minecraft/modpacks/create-chronicles-bosses-and-beyond)

## Быстрая установка через git

```powershell
cd %appdata%\.minecraft
git clone https://github.com/MatveiShadchin/create-chronicles-host-fix.git temp-cc-fix
xcopy /E /I /Y temp-cc-fix\kubejs kubejs
xcopy /E /I /Y temp-cc-fix\defaultconfigs defaultconfigs
rmdir /S /Q temp-cc-fix
```
