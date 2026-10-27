# 🏕️ Server Emulation For Talking Tom Camp

> *"Start filling your balloons, we are almost at the camp. The adventure is about to begin!"*

<p align="center">
  <img src="https://img.shields.io/badge/Status-In_Development-yellow?style=for-the-badge" alt="Status"/>
  <img src="https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android"/>
  <img src="https://img.shields.io/badge/Server_Emulation-purple?style=for-the-badge" alt="Server Emulation"/>
  <img src="https://img.shields.io/badge/Private_Server-orange?style=for-the-badge" alt="Private Server"/>
  <img src="https://img.shields.io/badge/Progress-Breakthrough!-brightgreen?style=for-the-badge" alt="Progress"/>
  <img src="https://img.shields.io/badge/License-AGPL_v3-blue?style=for-the-badge&logo=gnu&logoColor=white" alt="License: AGPL v3"/>
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
| Server response format is fully cracked | ✅/🟡 (JSON-keys ✅, their meaning 🟡) |
| Fix configuration bugs / Build full server emulator **PROTOTYPE** for most essential URLs | 🟡 In progress |
| Build full server emulator **PROTOTYPE** for **ALL** URLs | 🔜 Not for now, coming soon |
| Build full server emulator **RELEASE** version / **SOFTWARE** version | 🔜 Coming soon |
| Build full server emulator **MOBILE PORT** version | 🔜 Coming soon |
| **RELEASE** | 🔜 Coming soon |
| **Private server** **SOFTWARE** release | 🔜 Coming soon |
| **MY OWN** private server | ❓ |

---

## 📚 Additional Info

<details>
<summary><b>🐛 Game bugs with the server emulator (will be removed)</b></summary>

There are so many for now!
1. Incorrect balancing (incorrect hp, radius, etc on units, buildings)
2. Game crashes on some parts (not some, the game is just **UNPLAYABLE** for now)
3. Unknown future about clans, pvp, notifications

</details>

<details>
<summary><b>ℹ️ General information</b></summary>

For now, server emulator is on python (mitmproxy), also GO server (i don't know for what) and apps-ext.outfit7.com redirect in system/etc/hosts.
The testing is on LDPlayer 9 (not an ad, huh?). Current Talking Tom Camp is modified for removing SSL pinning.
I started this project around 30th may 2026, but started documenting recently.
The school eats my time, so I can't devote much time to this project.
The idea of reviving Talking Tom Camp occurred to me only in 2026. Before 2026, I just searched in internet private server and hoped it exists, but my patience snapped.
I don't know when i will publish first server emulator, just wait some time!
And also about **MOBILE PORT**, i will try to make like launcher, where you can download any version of talking tom camp, this app will modify version to make the game server emulating/private server ready, and you will have opportunity not only to play alone, but also play on local network and even join **PRIVATE SERVER**! And also, the emulator not only will can be to make game working, but also simulate server errors, you will also can to modify balance of the game, and (i think) even turn on debug mode if it's will be possible! And i think playing with debug mode will be interesting because of it's potential.

</details>

<details>
<summary><b>🖥️ About the server emulator / private server</b></summary>

Nothing to say yet, wait some time!

</details>

<details>
<summary><b>📞Contacts</b></summary>

So, I have telegram: @ianesnaychtotytnapisat

And also, I have a discord server (English only):
https://discord.gg/r5M2ruZ9Kr

That's all for now!

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

<details>
<summary><b>UPD6 — Real progress, architectural limits, and future plans 👀</b></summary>

Okay, a lot has happened since UPD5. The game is **actually becoming playable**, not just launching:

**What works now:**
- ✅ Nicknames
- ✅ Coupons
- ✅ Fights 
- ✅ ...and more

**What's still broken (and there's a lot):**
- 🐛 Units deal damage incorrectly in battle (some insta-kill, some deal zero damage)
- 🐛 Building upgrades don't work at all
- 🐛 Training/building timers don't tick
- 🐛 Visual bugs
- 🐛 ...and more

> 💭 **A quick note on "original gameplay":** Since the original servers used a "dumb" architecture, all the balancing data (unit damage, HP, timers) lived on Outfit7's servers, which are gone forever. The client only knows the JSON structure. So, to recover the "original gameplay", I would need a traffic dump from before the server shutdown OR meticulously watch old gameplay videos and try to reverse-engineer the numbers from them. But even then, it will not be 100% original no matter what. I am rebuilding the logic from scratch.

**About "other revivals":** I've seen another project claiming to bring TTC back. It has a website and a YouTube video. But if you look closely at their progress, they have no actual APK released yet, and their development seems to be quite unstable. Oh, and they mentioned in their video that if they don't get enough donations, the project will become **paid**. I'm doing this **for free, in the open, and mostly solo**. I'm not here to compete. If they actually deliver something working — good for them. But for now, I'll stick to fixing my own bugs. 🐛

**Future plans (Launcher & Anti-Cheat):**
I also plan to build a launcher/mobile port. This app will not only let you easily patch the game for server emulation but will also try to patch the holes Outfit7 left behind. I want to add server-side validation so you can't just use Game Guardian to conjure 99999 gems and instantly break the economy. Yes, it's a cat-and-mouse game, but I'll try to make it fair.

**A note on the team:** Right now, I'm doing this completely **solo**. Even with a bunch of fans waiting (thank you!), it's hard to find someone as crazy as me to spend this much time and effort. Most will just wait. But I'll keep trying to find at least 1-2 enthusiasts to help out with specific tasks.

**P.S.** I already have some early emulator builds! They are not public on GitHub yet, but they are available on my Discord server along with an installation guide. The server is mostly English-speaking, but you are welcome to join!

</details>

## 📄 License

This project is licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**.

- ✅ You are free to use, modify, and distribute this software.
- ✅ If you run a modified version **on a network server** and let others use it, you **must** release your source code under the same license.
- ❌ You cannot use this code in closed-source or proprietary projects.

See the full text in the [`LICENSE`](LICENSE) file.

> **Note:** The AGPL-3.0 license applies **only to the code in this repository**, not to any assets or content belonging to Outfit7 Limited.

---

## ⚖️ Disclaimer

This project is a **fan-made server emulator** and is **not affiliated with, endorsed by, or associated with Outfit7 Limited** in any way.

- **Talking Tom Camp**, all related characters, assets, trademarks, and copyrights belong to **Outfit7 Limited**.
- This project is **non-commercial** and made **for preservation and educational purposes only**.
- No original game files, assets, or copyrighted content are distributed in this repository.
- **Client modification:** This project does **not** distribute any modified game clients (APKs). Any necessary client-side modifications are provided as **separate tools, patches, or instructions** and are intended for use **only on legally obtained copies of the game** for preservation purposes. Users apply them at their own risk.
- All trademarks and copyrights are the property of their respective owners.

If you are a representative of Outfit7 and have concerns about this project, please contact me and I will take appropriate action.

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
  <img src="https://img.shields.io/badge/Лицензия-AGPL_v3-blue?style=for-the-badge&logo=gnu&logoColor=white" alt="Лицензия: AGPL v3"/>
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
| Формат ответа сервера полностью разгадан | ✅/🟡 (JSON-ключи ✅, их значение 🟡) |
| Исправление багов конфигурации / Создание **ПРОТОТИПА** полноценного эмулятора сервера для самых важных URL | 🟡 В процессе |
| Создание **ПРОТОТИПА** полноценного эмулятора сервера для **ВСЕХ** URL | 🔜 Пока не сейчас, скоро |
| Создание **РЕЛИЗ** версии эмулятора сервера / версии как **ПО** | 🔜 Скоро |
| Создание **МОБИЛЬНОГО ПОРТА** эмулятора сервера | 🔜 Скоро |
| **РЕЛИЗ** | 🔜 Скоро |
| Релиз **ПО** для **приватного сервера** | 🔜 Скоро |
| **МОЙ СОБСТВЕННЫЙ** приватный сервер | ❓ |

---

### 📚 Дополнительная информация

<details>
<summary><b>🐛 Баги игры с эмулятором сервера (будут удалены)</b></summary>

Их пока что очень много!
1. Неправильный баланс (неправильные хп, радиус и т.д. у юнитов, зданий)
2. Игра крашится в некоторых местах (не в некоторых, игра просто **НЕИГРАБЕЛЬНА** пока что)
3. Неизвестное будущее насчёт кланов, пвп, уведомлений

</details>

<details>
<summary><b>ℹ️ Общая информация</b></summary>

Пока что эмулятор сервера на Python (mitmproxy), ещё GO-сервер (я не знаю для чего) и редирект apps-ext.outfit7.com в system/etc/hosts.
Тестирование идёт на LDPlayer 9 (не реклама, хах). Текущий Говорящий Том: Водная битва модифицирован для удаления SSL pinning.
Я начал этот проект где-то 30 мая 2026, но документировать начал недавно.
Школа съедает моё время, так что я не могу уделять проекту много времени.
Идея возродить Говорящий Том: Водная битва пришла ко мне только в 2026. До 2026 я просто искал в интернете приватный сервер и надеялся, что он существует, но моё терпение лопнуло.
Я не знаю когда выпущу первый эмулятор сервера, просто подождите немного!
И ещё насчёт **МОБИЛЬНОГО ПОРТА**: я попробую сделать типа лаунчер, где вы можете скачать любую версию говорящего тома, это приложение будет модифицировать версию, чтобы игра была готова к эмуляции сервера/приватному серверу, и у вас будет возможность не только играть одному, но и играть по локалке и даже присоединиться к **ПРИВАТНОМУ СЕРВЕРУ**! А ещё, эмулятор не только сможет заставить игру работать, но и симулировать серверные ошибки, вы также сможете изменять баланс игры, и (я думаю) даже включить дебаг-режим если это будет возможно! И я думаю играть с дебаг-режимом будет интересно из-за его потенциала.

</details>

<details>
<summary><b>🖥️ Об эмуляторе сервера / приватном сервере</b></summary>

Пока что нечего сказать, подождите немного!

</details>

<details>
<summary><b>📞Контакты</b></summary>

У меня есть telegram: @ianesnaychtotytnapisat

И также, есть discord сервер (Там только англичане, но рады всем!):
https://discord.gg/r5M2ruZ9Kr

Это всё на данный момент!

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

<details>
<summary><b>АПД6 — Реальный прогресс, ограничения архитектуры и планы на будущее 👀</b></summary>

Короче, с момента АПД5 много всего произошло. Игра **реально становится играбельной**, а не просто запускается (ну хотяяя, про играбельность прям загнул):

**Что уже работает:**
- ✅ Ники
- ✅ Купоны
- ✅ Бои
- ✅ ...и другое

**Что ещё сломано (и этого много):**
- 🐛 Юниты неправильно наносят урон в бою (некоторые моментально убивают, некоторые вообще не наносят дамага)
- 🐛 Апгрейды зданий вообще не работают
- 🐛 Таймеры тренировки/постройки не идут
- 🐛 Визуальные баги
- 🐛 ...и это ещё не всё

> 💭 **Небольшое примечание насчёт "оригинального геймплея":** Так как оригинальные серверы использовали "тупую" архитектуру, все данные баланса (урон юнитов, ХП, таймеры) жили на серверах Outfit7, которых больше нет. Клиент знает только структуру JSON. Поэтому, чтобы восстановить "оригинальный геймплей", мне нужен либо дамп трафика до закрытия серверов, либо нужно пересматривать тонны геймплейных видео и пытаться вытащить цифры оттуда. Но даже в этом случае это не будет на 100% оригинально, как бы я ни старался. Я восстанавливаю логику с нуля.

**Насчёт "других возрождений":** Я видел еще один проект, который обещает вернуть TTC. У него есть сайт и видео на ютубе. Но если посмотреть на их прогресс поближе, у них до сих пор нет выпущенного APK, и разработка выглядит довольно нестабильно. А ещё они упомянули в своём видео, что если не наберут достаточно донатов, то их проект станет **платным**. Я делаю это **бесплатно, открыто и в основном в одиночку**. Я здесь не для конкуренции. Если они реально выпустят что-то рабочее — круто. Но пока что я буду чинить свои баги. 🐛

**Планы на будущее (Лаунчер и защита от читов):**
Я также планирую сделать лаунчер/мобильный порт. Это приложение не только позволит легко патчить игру для эмуляции сервера, но и попытается залатать дыры, которые оставили Outfit7. Я хочу добавить серверную валидацию, чтобы нельзя было просто через Game Guardian наколдовать 99999 гемов и мгновенно сломать экономику. Да, это игра в кошки-мышки, но я постараюсь сделать игру честной.

**Насчёт команды:** Прямо сейчас я делаю это полностью **в одиночку**. Даже с кучей ожидающих фанатов (спасибо вам!), сложно найти такого же сумасшедшего, как я, готового тратить столько времени и сил. Большинство просто будет ждать. Но я продолжу искать хотя бы 1-2 энтузиастов, чтобы помочь с конкретными задачами.

**P.S.** У меня уже есть ранние сборки эмулятора! Они пока не выложены публично на GitHub, но доступны на моём Discord-сервере вместе с инструкцией по установке. Сервер в основном англоязычный, но я буду рад, если вы зайдёте!

Скорей всего, на этом закончится лог об разработке. Позже уже будут релизы и информация о них.

</details>

### 📄 Лицензия

Этот проект распространяется под лицензией **GNU Affero General Public License v3.0 (AGPL-3.0)**.

- ✅ Вы можете свободно использовать, изменять и распространять этот код.
- ✅ Если вы запускаете изменённую версию **на сервере** и даёте к ней доступ по сети — вы **обязаны** открыть исходный код под той же лицензией.
- ❌ Запрещено использовать этот код в закрытых или проприетарных проектах.

Полный текст — в файле [`LICENSE`](LICENSE).

> **Примечание:** лицензия AGPL-3.0 распространяется **только на код в этом репозитории**, но не на ассеты или контент, принадлежащие Outfit7 Limited.

---

### ⚖️ Дисклеймер

Этот проект — **фанатский эмулятор сервера**, и он **никак не связан с Outfit7 Limited**, не одобрен и не аффилирован с ней.

- **Говорящий Том: Водная битва**, все связанные персонажи, ассеты, торговые марки и авторские права принадлежат **Outfit7 Limited**.
- Проект является **некоммерческим** и создан **исключительно в целях сохранения игры и обучения**.
- В этом репозитории **не распространяются** оригинальные игровые файлы, ассеты или защищённый авторским правом контент.
- **Модификация клиента:** этот проект **не распространяет** модифицированные клиенты игры (APK). Все необходимые изменения на стороне клиента предоставляются в виде **отдельных инструментов, патчей или инструкций** и предназначены **только для использования на легально полученных копиях игры** в целях сохранения. Пользователи применяют их на свой страх и риск.
- Все торговые марки и авторские права принадлежат их соответствующим владельцам.

Если вы являетесь представителем Outfit7 и у вас есть вопросы по этому проекту — свяжитесь со мной, и я предприму соответствующие меры.

---

<p align="center">
  <i>Сделано с ❤️ для игры, которая заслуживала лучшего.</i><br>
  <sub>⭐ Поставь звёздочку репозиторию, если хочешь снова увидеть Говорящий Том: Водная битва живым!</sub>
</p>

</details>

---
