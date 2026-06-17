# 🚀 Space Ship Survivor — Assets Edition

**Space Ship Survivor** — браузерная 2D arcade/survivor-игра на чистом **HTML + CSS + JavaScript Canvas**.  
Игрок управляет космическим кораблём, выживает против волн врагов, собирает XP, открывает достижения, прокачивает корабли и усиливает ангар после каждого забега.

Проект сделан как **MVP survivor-игры**, которую можно запускать прямо в браузере без сборщиков, фреймворков и серверной части.

---

## 🎮 Gameplay

Игрок появляется на космической арене и должен выживать как можно дольше.  
Во время забега нужно:

- уничтожать астероиды, дронов и боссов;
- собирать XP и Scrap;
- повышать уровень корабля;
- выбирать временные апгрейды;
- выполнять миссии;
- использовать активный навык корабля;
- выживать до финального времени или играть в бесконечном режиме.

---

## ✨ Features

- ✅ Полностью браузерная игра на Canvas
- ✅ Один основной `index.html`
- ✅ Несколько игровых режимов
- ✅ Выбор корабля перед стартом
- ✅ Уникальные пассивные бонусы кораблей
- ✅ Активный навык на клавишу `E`
- ✅ Прокачка навыков кораблей
- ✅ Ангар постоянных улучшений
- ✅ XP, уровни, Scrap и достижения
- ✅ Боссы с отдельной полосой здоровья
- ✅ Миссии внутри забега
- ✅ Safe Zone и события на карте
- ✅ Настройки музыки и обучения
- ✅ Сохранение прогресса через `localStorage`
- ✅ Адаптивный HUD для desktop и mobile
- ✅ Поддержка внешних PNG assets
- ✅ Фоновая музыка через `music/background.mp3`

---

## 🕹️ Controls

| Action | Key |
|---|---|
| Move | `WASD` / Arrow Keys |
| Aim | Mouse |
| Keyboard Aim | `IJKL` |
| Boost | `Space` |
| Fire Mode / Overdrive | `Shift` |
| Active Skill | `E` |
| Pause | `Esc` / `P` |

---

## 🚀 How to Run

### Option 1 — Open directly

You can open `index.html` directly in the browser.

```bash
index.html
```

### Option 2 — Run with local server

Recommended for assets and audio loading:

```bash
npx serve .
```

or

```bash
python -m http.server 8080
```

Then open:

```bash
http://localhost:8080
```

---

## 📁 Project Structure

```txt
space-ship-survivor/
├── index.html
├── README.md
├── music/
│   └── background.mp3
└── assets/
    ├── ships/
    │   ├── scout.png
    │   ├── tank.png
    │   ├── engineer.png
    │   ├── gunner.png
    │   └── phantom.png
    ├── enemies/
    │   ├── asteroid_small.png
    │   ├── asteroid_big.png
    │   ├── drone_fast.png
    │   ├── drone_sniper.png
    │   ├── mine.png
    │   ├── magnet.png
    │   └── shield.png
    ├── bosses/
    │   ├── scout_boss.png
    │   ├── laser_boss.png
    │   ├── asteroid_titan.png
    │   └── mothership.png
    ├── items/
    │   ├── xp.png
    │   ├── xp_rare.png
    │   ├── scrap.png
    │   ├── health.png
    │   └── energy.png
    ├── effects/
    │   ├── laser_cyan.png
    │   ├── laser_red.png
    │   ├── plasma_beam.png
    │   ├── explosion_small.png
    │   ├── explosion_big.png
    │   ├── shield_hit.png
    │   ├── level_up.png
    │   └── boost_flame.png
    └── ui/
        ├── upgrade_damage.png
        ├── upgrade_fire_rate.png
        ├── upgrade_shield.png
        ├── upgrade_speed.png
        ├── upgrade_magnet.png
        ├── upgrade_pierce.png
        ├── upgrade_crit.png
        ├── upgrade_regen.png
        ├── scrap_icon.png
        └── boss_warning.png
```

---

## 🚀 Ships

| Ship | Role | Description |
|---|---|---|
| Scout | Speed / Combo | Fast ship with dodge and longer combo window |
| Tank | Defense | High shield, lower damage taken, shockwave mechanics |
| Engineer | Support | Strong magnet, regeneration and longer zone effects |
| Gunner | Damage | Double laser, faster fire rate and stronger fire energy |
| Phantom | Mobility | Strong boost and reduced damage while boosting |

Each ship has:

- passive bonuses;
- unique playstyle;
- active skill;
- separate skill upgrade level.

---

## 🧠 Active Skills

| Ship | Skill | Effect |
|---|---|---|
| Scout | Dash | Fast dash through enemies |
| Tank | Shockwave | Pushes and damages enemies around the ship |
| Engineer | Repair Field | Creates a healing field |
| Gunner | Overload | Temporarily increases fire power |
| Phantom | Ghost Mode | Allows safer movement through enemies |

Skills can be upgraded in the hangar using Scrap.

---

## 🎯 Game Modes

| Mode | Description |
|---|---|
| Classic | Survive 10 minutes |
| Free Play | Endless survival mode |
| Boss Rush | Fight a chain of bosses |
| Mission Run | Complete a set of missions |
| Hardcore | Harder enemies, higher Scrap reward |
| Daily Challenge | More intense challenge-style run |

---

## 🏆 Progression

The game stores progress in the browser using `localStorage`.

Saved data includes:

- total Scrap;
- best survival time;
- selected ship;
- permanent hangar upgrades;
- skill upgrade levels;
- achievements;
- run statistics;
- settings.

Storage key:

```js
sss_assets_edition_v1
```

---

## 🔧 Hangar Upgrades

Permanent upgrades available in the hangar:

- Start Shield
- Base Damage
- Fire Rate
- Boost
- Magnet
- Scrap Recycling
- Ship Skill Upgrades

These upgrades remain after death and affect future runs.

---

## 🏅 Achievements

Achievements reward the player with bonus Scrap.  
Examples:

- First Launch
- First Minute
- Stable Pilot
- Hunter
- Boss Breaker
- Level 10
- Scrap Collector
- Survivor

---

## 🎵 Music

The game expects background music at:

```txt
music/background.mp3
```

You can change the music path inside the code:

```js
const MUSIC_URL = './music/background.mp3'
```

Browser audio starts only after the first user interaction because of browser autoplay restrictions.

---

## 🖼️ Assets

All images are loaded from the `assets` folder.  
If an image is missing, the game will still try to run, but that object may render without its intended sprite.

Recommended format:

- PNG with transparency
- Optimized WebP/PNG for production
- Small readable sprites
- Consistent top-down or arcade style

---

## 🛠️ Tech Stack

- HTML5
- CSS3
- JavaScript
- Canvas API
- LocalStorage
- Web Audio API
- No frameworks
- No build step

---

## 📌 Current Status

This project is currently an **MVP / prototype** version.

Implemented:

- core game loop;
- player movement;
- enemy spawning;
- shooting;
- upgrades;
- ships;
- modes;
- achievements;
- boss system;
- save system;
- HUD and menus.

---

## 🧩 Roadmap

Planned improvements:

- [ ] Split code into separate files
- [ ] Add better mobile controls
- [ ] Add more enemy types
- [ ] Add more boss attack patterns
- [ ] Add visual polish for explosions
- [ ] Add sound effects pack
- [ ] Add settings for volume
- [ ] Add language switcher
- [ ] Add PWA support
- [ ] Add leaderboard
- [ ] Add online co-op prototype
- [ ] Add build system with Vite
- [ ] Optimize assets for production

---

## 🌐 Deployment

You can deploy the project on:

- GitHub Pages
- Netlify
- Vercel
- Any static hosting

For GitHub Pages:

1. Push the project to GitHub.
2. Go to repository settings.
3. Open **Pages**.
4. Select branch `main`.
5. Select root folder `/`.
6. Save and wait for deployment.

---

## 📸 Screenshots

Add screenshots here after uploading images to the repository:

```md
![Main Menu](screenshots/menu.png)
![Gameplay](screenshots/gameplay.png)
![Hangar](screenshots/hangar.png)
```

---

## 👨‍💻 Author

Created by **Temirkhan Rustemov**.

---

## 📄 License

This project is open for learning, prototyping and further development.  
You can add your preferred license, for example:

```txt
MIT License
```
