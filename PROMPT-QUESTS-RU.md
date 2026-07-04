# Промпт для Cursor (для хоста — только русские квесты)

**Как пользоваться:**
1. Открой **Cursor**
2. **File → Open Folder** → выбери папку `%appdata%\.minecraft`  
   (в проводнике в адресной строке вставь `%appdata%\.minecraft` и Enter)
3. Создай **новый чат** (Agent)
4. Скопируй **весь текст ниже** (между линиями) и вставь в чат
5. Нажми Enter — агент сделает всё сам

---

```
Привет! Я хост в Minecraft — открываю мир для LAN, ко мне подключается второй игрок.

Сборка: Create Chronicles: Bosses and Beyond 2.5.3
Minecraft 1.20.1, Forge (TLauncher или CurseForge)

Мне нужно ТОЛЬКО поставить русский перевод квестов FTB Quests.
KubeJS, mods, saves, defaultconfigs — НЕ ТРОГАТЬ. Мир не удалять. Бэкап мира не обязателен (меняем только текст квестов).

Репозиторий с переводом:
https://github.com/MatveiShadchin/create-chronicles-host-fix

ZIP напрямую:
https://github.com/MatveiShadchin/create-chronicles-host-fix/archive/refs/heads/main.zip

Что нужно скопировать:
  quests-ru/config/ftbquests/quests/
  → в мою папку .minecraft/config/ftbquests/quests/
(заменить файлы внутри папки quests, не всю config)

Сделай всё сам, без лишних вопросов:

1. Найди папку Minecraft:
   - Обычно: %appdata%\.minecraft
   - Если CurseForge: ...\Instances\Create Chronicles Bosses and Beyond\minecraft
   - Используй ту, откуда реально запускается игра

2. Убедись, что Minecraft ЗАКРЫТ (нет javaw.exe в диспетчере задач)

3. Скачай репозиторий:
   - git clone https://github.com/MatveiShadchin/create-chronicles-host-fix.git во временную папку
   - ИЛИ скачай ZIP по ссылке выше и распакуй

4. Скопируй ТОЛЬКО папку quests из quests-ru:
   - Источник: .../quests-ru/config/ftbquests/quests/
   - Назначение: .minecraft/config/ftbquests/quests/
   - Должно получиться:
     • config/ftbquests/quests/chapters/ — 31 файл .snbt
     • config/ftbquests/quests/chapter_groups.snbt
     • config/ftbquests/quests/data.snbt

5. НЕ меняй ничего другого:
   - НЕ kubejs
   - НЕ mods
   - НЕ saves
   - НЕ defaultconfigs

6. Напиши короткий отчёт на русском:
   - Путь к .minecraft
   - Сколько файлов .snbt в chapters (ожидается 31)
   - Готово ли к запуску игры

7. Напомни мне в конце:
   - Полностью перезапустить Minecraft
   - Открыть мир и «Открыть для LAN»
   - Открыть книгу квестов — текст должен быть на русском
   - Если не обновилось: команда в чате /ftbquests reload

Если что-то пошло не так — опиши проблему и что делать вручную (3–5 шагов).
```

---

## Если агент спросит разрешение

Разреши выполнение команд (скачивание, копирование файлов).

## После установки

1. Запусти Minecraft (Forge 1.20.1)
2. Открой свой мир
3. **Esc → Открыть для LAN**
4. Открой книгу квестов — должно быть на русском

Второй игрок увидит русские квесты автоматически (квесты идут с хоста).

## Если квесты всё ещё на английском

В чате игры:
```
/ftbquests reload
```
Или полностью перезапусти мир.

---

**Ссылка на репозиторий:** https://github.com/MatveiShadchin/create-chronicles-host-fix
