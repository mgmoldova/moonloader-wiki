---
title: Системные события (Events) в MoonLoader
description: Справочник всех системных и сетевых событий Lua в MoonLoader. Сигнатуры функций, перехват пакетов, RPC и оконных сообщений.
---

# Системные события (Events)

**События** — это функции, которые вызываются движком MoonLoader автоматически при наступлении определённых условий в игре или системе. 

!!! info "Регистрация обработчиков"
    Обработчик системного события регистрируется путём объявления **глобальной функции** с соответствующим движку названием (например, `onScriptTerminate`). Все аргументы и возвращаемые значения событий являются опциональными.

---

## Список системных событий

| Версия | Сигнатура события (Ссылка на описание) | Категория |
| :---: | :--- | :--- |
| `v0.015` | [`main()`](events/main.md) | `системные` |
| `v0.015` | [`onQuitGame()`](events/onQuitGame.md) | `системные` |
| `v0.015` | [`onScriptLoad(LuaScript s)`](events/onScriptLoad.md) | `скрипты` |
| `v0.015` | [`onSystemInitialized()`](events/onSystemInitialized.md) | `системные` |
| `v0.015` | [`onScriptMessage(string msg, LuaScript s)`](events/onScriptMessage.md) | `сообщения` |
| `v0.015` | [`onSystemMessage(string msg, int type, LuaScript s)`](events/onSystemMessage.md) | `сообщения` |
| `v0.015` | [`bool process, int id, bitstream bitStream = onReceivePacket(int id, bitstream bitStream)`](events/onReceivePacket.md) | `сеть` `пакеты` |
| `v0.015` | [`bool process, int id, bitstream bitStream = onReceiveRpc(int id, bitstream bitStream)`](events/onReceiveRpc.md) | `сеть` `rpc` |
| `v0.015` | [`bool process, int id, bitstream bitStream, int priority, int reliability, int orderingChannel = onSendPacket(int id, bitstream bitStream, int priority, int reliability, int orderingChannel)`](events/onSendPacket.md) | `сеть` `пакеты` |
| `v0.015` | [`bool process, int id, bitstream bitStream, int priority, int reliability, int orderingChannel, bool shiftTs = onSendRpc(int id, bitstream bitStream, int priority, int reliability, int orderingChannel, bool shiftTs)`](events/onSendRpc.md) | `сеть` `rpc` |
| `v0.022` | [`onExitScript(bool quitGame)`](events/onExitScript.md) | `скрипты` |
| `v0.022` | [`onScriptTerminate(LuaScript s, bool quitGame)`](events/onScriptTerminate.md) | `скрипты` |
| `v0.022` | [`onWindowMessage(uint msg, uint wparam, int lparam)`](events/onWindowMessage.md) | `интерфейс` |
| `v0.023` | [`onStartNewGame(int mpack)`](events/onStartNewGame.md) | `игровые` |
| `v0.023` | [`onLoadGame(table saveData)`](events/onLoadGame.md) | `игровые` |
| `v0.023` | [`table newSaveData = onSaveGame(table saveData)`](events/onSaveGame.md) | `игровые` |

---

!!! tip "Перехват сетевого трафика"
    События `onReceivePacket`, `onReceiveRpc`, `onSendPacket` и `onSendRpc` позволяют полностью контролировать сетевой поток между клиентом и сервером. Возвращение значения `false` в начале этих функций (переменная `process`) полностью блокирует пакет или RPC, не давая игре или серверу узнать о его существовании.