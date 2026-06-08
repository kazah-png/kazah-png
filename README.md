<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:21262d&height=140&section=header&text=kazah-png&fontSize=52&fontColor=e6edf3&animation=fadeIn&fontAlignY=55" />
</div>

<div align="center">
  <strong>Python · Game automation · Computer vision · Systems engineering</strong>
  <br/><br/>
  <a href="https://github.com/kazah-png?tab=repositories">
    <img src="https://img.shields.io/badge/repositories-view%20all-0d1117?style=flat&logo=github&logoColor=white" />
  </a>
  <img src="https://komarev.com/ghpvc/?username=kazah-png&style=flat&color=161b22&label=profile+views" />
</div>

---

## About

I build automation systems at the intersection of computer vision, Android emulator control, and real-time decision making.
My main focus is game automation: full CV pipelines that run an ONNX inference model on each captured frame, classify game state through a priority-ordered state machine, and issue ADB commands back to the emulator — all inside a multi-threaded Python process with a desktop GUI and optional remote control via Discord or Telegram.

---

## Tech stack

**Language**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)

**Computer vision & AI**

![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![ONNX Runtime](https://img.shields.io/badge/ONNX%20Runtime-005CED?style=flat&logo=onnx&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)

**ONNX execution providers:** CUDA · DirectML · TensorRT · OpenVINO · CPU — selected at runtime based on hardware.

**Mobile / emulator control**

![ADB](https://img.shields.io/badge/ADB-3DDC84?style=flat&logo=android&logoColor=white)

Full ADB pipeline over TCP (`127.0.0.1:5555`). Screencap via `adb exec-out`, joystick via async `adb shell input swipe` (Popen), taps with joy-pause to preserve movement angle.

**Desktop GUI**

![CustomTkinter](https://img.shields.io/badge/CustomTkinter-1f6aa5?style=flat&logo=python&logoColor=white)

**Remote control**

![Discord](https://img.shields.io/badge/Discord%20bot-5865F2?style=flat&logo=discord&logoColor=white)
![Telegram](https://img.shields.io/badge/Telegram%20bot-2CA5E0?style=flat&logo=telegram&logoColor=white)

**Packaging & distribution**

![PyInstaller](https://img.shields.io/badge/PyInstaller-3776AB?style=flat&logo=python&logoColor=white)

Produces a standalone `.exe` with embedded models, configs, and assets. License validation at launch via a keygen bot and a TOML-based config.

**Algorithms**

A\* pathfinding · State machine (priority-ordered state classification) · Adaptive fog-avoidance · Wall-based unstuck detection with semicircle escape arc

---

## Projects

### KZH AI — Brawl Stars farming bot `private`

A closed Brawl Stars automation system built from scratch by combining and extending logic from several open-source bots. It operates entirely through ADB: captures emulator frames, runs an ONNX detector, classifies game state, and issues the appropriate ADB commands — all inside a single Python process.

**Architecture highlights**
- 23-module Python codebase (`main`, `detect`, `play`, `state_finder`, `stage_manager`, `adaptive_brain`, `pathfinding`, `lobby_automation`, `multi_worker`, `discord_control`, `telegram_control`, `trophy_observer`, `recovery_events`, `runtime_metrics`, …)
- Priority state machine: `offer_popup → team_invite → end_screen → star_drop → brawler_selection → matchmaking → lobby → in_game → unknown`
- Async joystick via `_adb_swipe_async()` + `_adb_tap_with_joy_pause()` to avoid pointer-0 conflicts
- Inactivity / idle-disconnect dialog auto-recovery
- Brawl Stars Developer Portal auto-key generation (logs in, detects current public IP, creates or reuses an API key) for trophy sync
- TOML-based config with hot-reload; `_toml_cache` with targeted invalidation
- CustomTkinter dashboard: hero banner, stat cards, live progress bars
- Discord and Telegram remote control (`/start`, `/stop`, `/status`, `/screenshot`, `/pause`, `/resume`)
- License screen + keygen bot; `dev_mode` bypass file for development
- PyInstaller single-exe distribution

**Results:** consistent ~57 % first-place rate in Trio Showdown; pushed multiple brawlers from 0 to 1 000 trophies unattended.

---

### PylaAi-XXZ — Open-source Brawl Stars bot fork `public`

A fork of [PylaAi](https://github.com/AngelFireLA/BrawlStarsBotMaking) focused on making Trio Showdown play correctly end-to-end. Contributions include:

- Analog joystick movement (continuous angle, not WASD taps) for smoother pathing and dodging
- Teammate-following with hysteresis to avoid ping-pong between nearby teammates
- Trio team spacing: orbit logic, bias-back-to-team, anti-stack
- Poison fog detection and flee-radius override
- Wall-based unstuck detector + alternating-side semicircle escape arc
- Place-based trophy tracking (1st / 2nd / 3rd / 4th end-screen recognition)
- One-click Windows setup helper (`setup.exe`): installs Python 3.11, pip deps, best available ONNX Runtime (CPU / DirectML / CUDA)
- Brawl Stars Developer Portal trophy autofill
- `Push All 1k` mode: sorts brawlers by least trophies, builds a full queue, farms unattended

> *"Currently the best external Brawl Stars bot."* — PylaAi-XXZ README

---

## GitHub stats

<div align="center">
  <img height="160" src="https://github-readme-stats.vercel.app/api?username=kazah-png&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=e6edf3&text_color=8b949e&icon_color=3fb950&count_private=true" />
  <img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=kazah-png&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=e6edf3&text_color=8b949e&layout=compact&langs_count=6" />
</div>

<div align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=kazah-png&theme=github-compact&bg_color=0d1117&color=8b949e&line=3fb950&point=3fb950&hide_border=true" />
</div>

---

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:21262d,50:161b22,100:0d1117&height=80&section=footer" />
</div>
