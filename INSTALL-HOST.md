# Установка для хоста (девушка / LAN-сервер)

Сборка: **Create Chronicles: Bosses and Beyond 2.5.3**, Minecraft **1.20.1**, Forge **47.3.0**.

## Скачать

**ZIP:** https://github.com/MatveiShadchin/create-chronicles-host-fix/archive/refs/heads/main.zip

**Или git:**
```powershell
git clone https://github.com/MatveiShadchin/create-chronicles-host-fix.git
```

## Шаг 1 — Бэкап мира

Скопируй папку мира:
```
%appdata%\.minecraft\saves\ИМЯ_МИРА
→ saves\ИМЯ_МИРА_backup
```

## Шаг 2 — Закрой Minecraft полностью

Не просто выйти из мира — закрыть игру и лаунчер.

## Шаг 3 — Скопируй файлы

Открой `%appdata%\.minecraft` и скопируй из распакованного репозитория:

| Из репозитория | Куда в .minecraft |
|----------------|-------------------|
| `kubejs\` | `kubejs\` (заменить целиком) |
| `defaultconfigs\` | `defaultconfigs\` (заменить целиком) |
| `quests-ru\config\ftbquests\quests\` | `config\ftbquests\quests\` (заменить папку quests) |

## Шаг 4 — Запусти игру

1. TLauncher → **Forge 1.20.1**
2. Открой мир (ты — хост, «Открыть для LAN»)
3. Второй игрок подключается к тебе

## Шаг 5 — Проверка

| Что проверить | Как |
|---------------|-----|
| KubeJS работает | JEI → поиск **Rotation Mechanism** |
| Квесты на русском | Книга квестов → текст на русском |
| Логи | `.minecraft\logs\kubejs\startup.log` → есть `launch.js`, `main.js` |

Если квесты не обновились: `/ftbquests reload` или перезапуск мира.

## Важно

- **Хост обязан** иметь эти файлы — без kubejs на хосте предметы не работают у всех.
- **Второй игрок** тоже должен поставить `kubejs`, `defaultconfigs` и русские квесты.
- RAM: **8 GB** минимум.
- Forge: **47.3.0** (как в сборке).

## Быстрая установка одной командой (PowerShell)

```powershell
$mc = "$env:APPDATA\.minecraft"
$zip = "$env:TEMP\cc-host-fix.zip"
Invoke-WebRequest "https://github.com/MatveiShadchin/create-chronicles-host-fix/archive/refs/heads/main.zip" -OutFile $zip
Expand-Archive $zip "$env:TEMP\cc-host-fix" -Force
$src = "$env:TEMP\cc-host-fix\create-chronicles-host-fix-main"
Copy-Item "$src\kubejs" "$mc\kubejs" -Recurse -Force
Copy-Item "$src\defaultconfigs" "$mc\defaultconfigs" -Recurse -Force
Copy-Item "$src\quests-ru\config\ftbquests\quests" "$mc\config\ftbquests\quests" -Recurse -Force
Write-Host "Готово! Перезапусти Minecraft."
```
