# Промпт для Cursor (вставить на ПК хоста)

Скопируй всё между линиями и вставь в новый чат Cursor. Сначала открой папку `.minecraft` через File → Open Folder.

---

```
Ты на ПК хоста Minecraft. Сборка: Create Chronicles: Bosses and Beyond 2.5.3, Minecraft 1.20.1, Forge 47.3.0.

Задача: установить фикс KubeJS, чтобы работали квестовые предметы (rotation_mechanism и др.). Без kubejs JEI не находит эти предметы.

Репозиторий с файлами:
https://github.com/MatveiShadchin/create-chronicles-host-fix

Сделай ВСЁ сам, по шагам:

1. Найди папку Minecraft:
   - Обычно: %appdata%\.minecraft
   - Или CurseForge: ...\Instances\Create Chronicles Bosses and Beyond\minecraft
   - Открой ту, откуда реально запускается игра с этой сборкой.

2. СДЕЛАЙ БЭКАП мира перед любыми изменениями:
   - Скопируй папку saves\ИМЯ_МИРА в saves\ИМЯ_МИРА_backup_ДАТА

3. Скачай репозиторий:
   - git clone https://github.com/MatveiShadchin/create-chronicles-host-fix.git во временную папку
   - ИЛИ скачай ZIP с GitHub (Code → Download ZIP) и распакуй

4. Установи файлы:
   - Замени папку kubejs в .minecraft на kubejs из репозитория (658 файлов)
   - Замени/дополни папку defaultconfigs в .minecraft
   - Скопируй quests-ru/config/ftbquests/quests/ → config/ftbquests/quests/ (русские квесты, 31 глава)
   - Удали старые example.js если остались единственными скриптами — после установки должны быть launch.js, main.js, loot.js и др.

5. Проверь установку:
   - В kubejs\startup_scripts должны быть: launch.js, fluids.js, worldgenRemove.js
   - В kubejs\server_scripts должны быть: main.js, loot.js, misc_recipes.js и др.
   - Должна быть текстура: kubejs\assets\kubejs\textures\item\rotation_mechanism.png
   - В config\ftbquests\quests\chapters — 31 файл .snbt на русском
   - НЕ должно быть ситуации когда только example.js в startup_scripts

6. НЕ удаляй папку saves, mods, config целиком — только замена kubejs и defaultconfigs.

7. Напиши отчёт:
   - Путь к .minecraft
   - Сколько файлов в kubejs
   - Бэкап мира сделан или нет
   - Что осталось сделать вручную (перезапуск игры)

Важно:
- Полный перезапуск Minecraft обязателен (/reload не поможет для новых предметов)
- Forge лучше 47.3.0 как в сборке
- RAM 6-8 GB
- Второй игрок тоже должен иметь такой же kubejs

Не спрашивай разрешения на каждый шаг — выполни всё, что можешь, и отчитайся.
```

---
