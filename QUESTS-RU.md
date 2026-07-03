# Русификация квестов Create Chronicles

## Масштаб

- **31 глава**, ~**1400** названий квестов, ~**60 000** строк текста
- Официального русификатора **нет**
- Уже переведено: **Глава I** + названия групп глав

## Как применить перевод (Глава I)

Скопируй из папки `quests-ru/config/ftbquests/quests/` в свою `.minecraft/config/ftbquests/quests/`:

- `chapters/chapter_i_the_andesite_machine.snbt`
- `chapter_groups.snbt`

В игре: `/ftbquests reload` или перезапуск мира.

## Как перевести ВСЕ квесты (рекомендуемый способ)

### Вариант A — мод FTB Quest Localizer (проще всего)

1. Скачай [FTB Quest Localizer](https://www.curseforge.com/minecraft/mc-mods/ftb-quest-localizer) для **1.20.1**
2. Положи jar в `mods`, запусти игру
3. В чате: `/ftblang export en_us`
4. Мод создаст папку `FTBLang` с `en_us.json`
5. Переименуй копию в `ru_ru.json` и переведи значения на русский
6. Положи `ru_ru.json` в `kubejs/assets/kubejs/lang/` (если мод так настроит)
7. Перезапусти игру

### Вариант B — правка .snbt напрямую (как Глава I)

Текст в файлах `config/ftbquests/quests/chapters/*.snbt` — поля `title`, `subtitle`, `description`.

Плюс: работает сразу, без модов.  
Минус: много файлов, нужно переводить вручную или через Cursor.

## Промпт для Cursor (перевод оставшихся глав)

```
Переведи на русский файл квестов FTB Quests:
config/ftbquests/quests/chapters/ИМЯ_ФАЙЛА.snbt

Правила:
- Переводи только title, subtitle, description, tasks[].title
- НЕ трогай id, item, type, координаты, dependencies
- Сохрани форматирование Minecraft: &6, &r, &l, &o, &c, &a, &b, &e
- Сохрани JSON в description (clickEvent и т.д.) — переводи только text внутри
- Названия предметов из модов не переводи (create:andesite_alloy и т.д.)
- Стиль: дружелюбный, как в оригинале сборки
- Глава I уже переведена — используй как образец: chapter_i_the_andesite_machine.snbt
```

| Файл | Статус |
|------|--------|
| Все 31 глава + data.snbt + chapter_groups | ✅ Переведено (авто-перевод, июль 2026) |
| Резервная копия EN | `config/ftbquests/quests_backup_en/` |

## Применить все переводы

Скопируй папку `quests-ru/config/ftbquests/quests/` целиком в `.minecraft/config/ftbquests/quests/` (замени файлы).

В игре: `/ftbquests reload` или перезапуск мира.

## Как перевести ВСЕ квесты (если нужно обновить)
