# 🏕️ Server Emulation For Talking Tom Camp

> *"Start filling your balloons, we are almost at the camp. The adventure is about to begin!"*

<p align="center">
  <img src="https://img.shields.io/badge/Status-In_Development-yellow?style=for-the-badge" alt="Status"/>
  <img src="https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android"/>
  <img src="https://img.shields.io/badge/Server_Emulation-purple?style=for-the-badge" alt="Server Emulation"/>
  <img src="https://img.shields.io/badge/Private_Server-orange?style=for-the-badge" alt="Private Server"/>
  <img src="https://img.shields.io/badge/Progress-Breakthrough!-brightgreen?style=for-the-badge" alt="Progress"/>
</p>

<p align="center">
  <b>🎮 Reviving a dead, abandoned and forgotten game.</b>
</p>

---

## 📖 About the project

I'm trying to build a **server emulator for Talking Tom Camp (TTC)** — a game whose original servers were shut down *forever*. My goal is to make the game work **exactly like it did before shutdown**.

I want to restore:
- 🔔 Notifications
- 🏆 Leaderboards
- 👥 Clans
- ⚔️ Matchmaking
- 🌐 Full online support

...all **without Outfit7 servers**, **without Ads SDK**, and **without Google services** — because I want this to be fully self-contained.

> ⏳ I don't know exactly when it'll be done, but I hope to publish a **prototype soon** — without any unnecessary extras, just the bare minimum to get the game running.

---

## 🚦 Roadmap

| Task | Status |
|------|--------|
| Find backend URLs | ✅ Done |
| HTTP/HTTPS stub | ✅ Done |
| Server response format is (a little bit) cracked | ✅ Done |
| Game launches | ✅ **Working!** |
| Server response format is fully cracked | 🟡 In progress |
| Fix configuration bugs / Build full server emulator for all URLs | 🟡 In progress |
| Server emulator release | 🔜 Coming soon |
| Private server software release | 🔜 Coming soon |
| MY OWN private server | ❓ |

---

## 📚 Additional Info

<details>
<summary><b>🐛 Game bugs with the server emulator</b></summary>

Sorry, but there's nothing here yet. It'll be filled in soon, I promise!

</details>

<details>
<summary><b>ℹ️ General information</b></summary>

Sorry, but there's nothing here yet. It'll be filled in soon, I promise!

</details>

<details>
<summary><b>🖥️ About the server emulator / private server</b></summary>

Sorry, but there's nothing here yet. It'll be filled in soon, I promise!

</details>

---

## 📜 Development Log

<details>
<summary><b>UPD1 — Backend URLs found</b> <i>(outdated)</i></summary>

**Good news:** I found the TTC backend URLs and even made a stub — the *"LOGIN FAILED"* message is gone.

**Bad news:** Now there's a new message — *"CONNECTION ERROR"*.

![CONNECTION ERROR](https://github.com/Alexey19483/Server-Emulation-For-Talking-Tom-Camp/blob/0443aedc108afe94ca7d3a3ffc25dbaa4a52fd67/stubs/images/CONNECTION%20ERROR.png?raw=true)

</details>

<details>
<summary><b>UPD2 — Two possible paths</b> <i>(outdated)</i></summary>

Since TTC uses a custom engine — **Starlite** — there may be two versions:

1. 🎯 **Original TTC with server emulation** — online over local network and global internet. I might not host a global server, but I'll release the software so you can host your own.
2. 🔄 **TTC remade in another engine** — using the original assets. This version may or may not happen, but I could try.

</details>

<details>
<summary><b>UPD3 — Getting closer</b> <i>(outdated)</i></summary>

I didn't find anyone to help, so I'm still working solo. In short — I almost got it running. I managed to extract the **Grid config** through a hole in the server, but the game still lacks something.

Either something's wrong with the Google part, or there are hidden connections crashing the game, or I'm feeding the config to the game incorrectly *(though I got proper stubs working for other Outfit7 games)*. Anyway — I'll keep working.

</details>

<details>
<summary><b>UPD4 — HTTP(S) stub done, DTLS puzzle appears</b> <i>(outdated)</i></summary>

The HTTP(S) stub is ready, but it needs further refinement: live mode for the grid config, more URLs, etc. It's written in **Python with mitmproxy**.

**BUT EVEN WITH THE STUB, THE GAME DOESN'T START!**

Then I remembered something: in the game's code I saw mentions of **DTLS**, and in connections *(checked via PCAPDroid)* I saw weird-looking DNS (UDP) traffic. So I thought I'd need a DTLS stub.

> ⚠️ **SPOILER:** I know *nothing* about DTLS.

I'll take a little rest, learn DTLS, and then write the stub. It'll most likely also be in Python.

</details>

<details>
<summary><b>UPD4.5 — False alarm on DTLS</b> <i>(outdated)</i></summary>

Turns out `apps-ext.outfit7.com` (the main TTC server) is actually **HTTP**, not DTLS — so everything I said about DTLS was a jump to conclusions.

I'm now digging into this `apps-ext` server, and **possibly**, once I finally get the game running, I'll add UPD5 or UPD6 — and release the very first server emulator.

</details>

<details>
<summary><b>UPD5 — THE GAME IS FINALLY WORKING! 🎉</b></summary>

# 🎉 THE GAME IS FINALLY WORKING!!!

<p align="center">
  <img src="https://raw.githubusercontent.com/Alexey19483/Server-Emulation-For-Talking-Tom-Camp/refs/heads/Server-Emulation/stubs/images/photo_2026-09-26_23-32-22.jpg" width="30%" />
  <img src="https://raw.githubusercontent.com/Alexey19483/Server-Emulation-For-Talking-Tom-Camp/refs/heads/Server-Emulation/stubs/images/photo_2026-09-26_23-33-33.jpg" width="30%" />
  <img src="https://raw.githubusercontent.com/Alexey19483/Server-Emulation-For-Talking-Tom-Camp/refs/heads/Server-Emulation/stubs/images/photo_2026-09-26_23-33-29.jpg" width="30%" />
</p>

**BUT IT'S VERY BUGGY!** 🐛

Soon I'll fix the bugs and publish the **FIRST SERVER EMULATOR**!!!

</details>

---

> 💭 **TO BE HONEST:** I don't know who will play. The fandom has already broken up, I think, and the game is old — it's been almost **6 years** since the servers shut down — and only now did I finally get around to this.

---

<p align="center">
  <i>Made with ❤️ for a game that deserved better.</i><br>
  <sub>⭐ Star the repo if you want to see TTC alive again!</sub>
</p>

---

<details>
<summary><b>🇷🇺 Русский перевод</b></summary>

## 🏕️ Эмуляция сервера для «Говорящий Том: Водная битва»

> *«Пора наполнять шарики водой, лагерь уже близко. Приключения вот-вот начнутся!»*

<p align="center">
  <img src="https://img.shields.io/badge/Статус-В_разработке-yellow?style=for-the-badge" alt="Статус"/>
  <img src="https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android"/>
  <img src="https://img.shields.io/badge/Эмуляция_сервера-purple?style=for-the-badge" alt="Эмуляция сервера"/>
  <img src="https://img.shields.io/badge/Приватный_сервер-orange?style=for-the-badge" alt="Приватный сервер"/>
  <img src="https://img.shields.io/badge/Прогресс-Прорыв!-brightgreen?style=for-the-badge" alt="Прогресс"/>
</p>

<p align="center">
  <b>🎮 Возрождаю мертвую, заброшенную и забытую игру.</b>
</p>

### 📖 О проекте

Я пытаюсь сделать эмулятор сервера для «Говорящий Том: Водная битва» *(сокращённо — TTC; также известна как Битва Тома / Том Водная Битва / Лагерь Тома)*. Я делаю это потому, что оригинальный сервер уже выключен *(«спасибо», Outfit7!)*.

Я постараюсь сделать игру рабочей такой, какой она была до выключения серверов. Я попытаюсь восстановить всё:
- 🔔 Уведомления
- 🏆 Лидерборды
- 👥 Кланы
- ⚔️ Матчмейкинг
- 🌐 Полную поддержку онлайна

...без серверов Outfit7, без рекламных SDK и без всяких Google-штук — потому что я хочу **автономность**.

> ⏳ Я не знаю, когда всё будет готово, но надеюсь скоро выпустить первый прототип — без всего лишнего, то есть без того, что не нужно для запуска.

---

### 🚦 План работ

| Задача | Статус |
|--------|--------|
| Найти backend-адреса | ✅ Готово |
| HTTP/HTTPS-заглушка | ✅ Готово |
| Формат ответа сервера (немного) разгадан | ✅ Готово |
| Запуск игры | ✅ **Работает!** |
| Формат ответа сервера полностью разгадан | 🟡 В процессе |
| Исправление багов конфигурации / Создание полноценного эмулятора сервера для всех URL | 🟡 В процессе |
| Релиз эмулятора сервера | 🔜 Скоро |
| Релиз ПО для приватного сервера | 🔜 Скоро |
| МОЙ СОБСТВЕННЫЙ приватный сервер | ❓ |

---

### 📚 Дополнительная информация

<details>
<summary><b>🐛 Баги игры с эмулятором сервера</b></summary>

Извиняюсь, но тут пока-что ничего нету. Скоро будет заполнено, обещаю!

</details>

<details>
<summary><b>ℹ️ Общая информация</b></summary>

Извиняюсь, но тут пока-что ничего нету. Скоро будет заполнено, обещаю!

</details>

<details>
<summary><b>🖥️ Об эмуляторе сервера / приватном сервере</b></summary>

Извиняюсь, но тут пока-что ничего нету. Скоро будет заполнено, обещаю!

</details>

---

### 📜 Дневник разработки

<details>
<summary><b>АПД1 — Найдены backend-адреса</b> <i>(устаревший)</i></summary>

**Хорошая новость:** я пофиксил *«LOGIN FAILED»*, и я знаю backend-адреса TTC.

**Плохая новость:** теперь другое сообщение — *«CONNECTION ERROR»*.

![CONNECTION ERROR](https://github.com/Alexey19483/Server-Emulation-For-Talking-Tom-Camp/blob/0443aedc108afe94ca7d3a3ffc25dbaa4a52fd67/stubs/images/CONNECTION%20ERROR.png?raw=true)

</details>

<details>
<summary><b>АПД2 — Два возможных пути</b> <i>(устаревший)</i></summary>

В связи с тем, что движок здесь кастомный — **Starlite**, возможно, будет две версии:

1. 🎯 **Исходная игра с эмуляцией сервера** — онлайн по локалке и по сети. Прямо по сети, конечно, возможно: я, может, и не буду хостить, но выложу ПО для эмуляции и поднятия своего сервера.
2. 🔄 **Игра, переделанная на другой движок** — но с исходными ассетами. Возможно, такой версии не будет, но в принципе можно сделать.

</details>

<details>
<summary><b>АПД3 — Уже ближе</b> <i>(устаревший)</i></summary>

Я так и не нашёл никого, продолжаю работу. Короче говоря — я почти смог запустить. Я смог получить **Grid-конфиг** через дыру в сервере, но игре всё ещё чего-то не хватает.

Либо что-то с Google-составляющей, либо есть какие-то скрытые соединения, из-за которых падает игра, либо я как-то не так преподношу игре конфиг *(хотя с другими играми Outfit7 я смог нормально сделать заглушку и запустить их)*. Короче, буду продолжать работу.

</details>

<details>
<summary><b>АПД4 — HTTP(S)-заглушка готова, появляется DTLS-загадка</b> <i>(устаревший)</i></summary>

HTTP(S)-заглушка для `apps.outfit7.com` уже готова, но в дальнейшем нужна доработка: добавление других URL, чтобы заглушка отвечала и на них. Моя заглушка сделана на **Python с mitmproxy**.

**НО ДАЖЕ С ЗАГЛУШКОЙ ДО ЗАПУСКА ИГРЫ НЕ ДОХОДИТ!**

И тут я вспомнил: в коде игры я видел упоминания **DTLS**, а ещё в соединениях *(я смотрел через PCAPDroid)* я видел DNS (UDP), которые выглядели слишком странно. И, походу, мне придётся делать DTLS-заглушку.

> ⚠️ **СПОЙЛЕР:** я вообще не шарю за DTLS.

Возьму небольшой отдых, начну изучать DTLS, а потом буду писать заглушку. DTLS-заглушка, скорее всего, тоже будет на Python.

</details>

<details>
<summary><b>АПД4.5 — Ложная тревога по DTLS</b> <i>(устаревший)</i></summary>

Короче, оказалось, что `apps-ext.outfit7.com` *(основной сервер TTC)* — вообще **HTTP**, а не DTLS. Так что всё, что я говорил про DTLS, — это я поспешил с выводами.

Сейчас уже разбираюсь с этим `apps-ext.outfit7.com`, и **возможно**, когда у меня наконец-то будет хоть как-то запускаться игра, я добавлю АПД5 или АПД6 — и уже выложу самый первый эмулятор сервера.

</details>

<details>
<summary><b>АПД5 — ИГРА НАКОНЕЦ-ТО РАБОТАЕТ! 🎉</b></summary>

# 🎉 ИГРА НАКОНЕЦ-ТО РАБОТАЕТ!!!

<p align="center">
  <img src="https://raw.githubusercontent.com/Alexey19483/Server-Emulation-For-Talking-Tom-Camp/refs/heads/Server-Emulation/stubs/images/photo_2026-09-26_23-32-22.jpg" width="30%" />
  <img src="https://raw.githubusercontent.com/Alexey19483/Server-Emulation-For-Talking-Tom-Camp/refs/heads/Server-Emulation/stubs/images/photo_2026-09-26_23-33-33.jpg" width="30%" />
  <img src="https://raw.githubusercontent.com/Alexey19483/Server-Emulation-For-Talking-Tom-Camp/refs/heads/Server-Emulation/stubs/images/photo_2026-09-26_23-33-29.jpg" width="30%" />
</p>

**НО ОНА ОЧЕНЬ БАГАННАЯ!**

Скоро я пофикшу баги и выложу **ПЕРВЫЙ ЭМУЛЯТОР СЕРВЕРА**!!!

</details>

---

> 💭 **ЕСЛИ ЧЕСТНО:** я не знаю, кто будет играть. Фандом уже распался вроде, игра старая — ну, уже почти 6 лет с закрытия прошло — а мои руки только сейчас добрались.

---

<p align="center">
  <i>Сделано с ❤️ для игры, которая заслуживала лучшего.</i><br>
  <sub>⭐ Поставь звёздочку репозиторию, если хочешь снова увидеть Говорящий Том: Водна Битва живым!</sub>
</p>

</details>

---
