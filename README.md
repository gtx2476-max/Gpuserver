# ServerCare

Плагин для Minecraft 1.21.8 (Purpur/Paper) — панель управления нагрузкой сервера.

## Возможности
- GUI-панель (`/servercare`, только OP): статистика TPS/MSPT/RAM, очистка дропа
  (в том числе завалы от аирдропов), убийство мобов, очистка мусора,
  выгрузка чанков, принудительный GC, автоочистка по расписанию.
- Веб-панель: `http://IP-сервера:8765` — пароль из `config.yml`.
- Автоочистка каждые N минут (настраивается).

## Сборка (GitHub Actions)
Просто запушь репозиторий — workflow `.github/workflows/build.yml` соберёт `ServerCare.jar`,
скачай его в Actions → Build → Artifacts.

## Установка
1. Положи `ServerCare.jar` в папку `plugins`.
2. Запусти сервер, открой `plugins/ServerCare/config.yml`, смени `web.password`.
3. `/servercare` в игре (только OP) или сайт `http://IP:8765`.

## Команды
- `/servercare` (алиасы `/sc`, `/laggpanel`) — открыть панель. Требует OP + право `servercare.admin`.

## Важно
- Очистка дропа удаляет **все** выброшенные предметы — игроки должны забрать лут до очистки.
- `unloadChunks` не трогает чанки рядом с игроками и force-loaded чанки.
