# Промпт для Cursor — только русские квесты

Скопируй в новый чат Cursor на ПК хоста. Открой папку `%appdata%\.minecraft`.

---

```
Ты на ПК хоста Minecraft. Сборка Create Chronicles 2.5.3, 1.20.1.

Нужно ТОЛЬКО установить русский перевод квестов FTB Quests. KubeJS трогать НЕ нужно.

Репозиторий: https://github.com/MatveiShadchin/create-chronicles-host-fix

Сделай сам:

1. Найди папку Minecraft: %appdata%\.minecraft

2. Скачай репозиторий (git clone или ZIP с GitHub)

3. Скопируй ТОЛЬКО:
   quests-ru/config/ftbquests/quests/
   → .minecraft/config/ftbquests/quests/
   (замени файлы в папке quests)

4. НЕ трогай kubejs, mods, saves, defaultconfigs.

5. Отчёт: путь к .minecraft, сколько .snbt файлов в chapters (должно быть 31), перезапуск игры вручную.

Проверка: книга квестов на русском. Если нет — /ftbquests reload.
```

---
