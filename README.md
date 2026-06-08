<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:21262d&height=140&section=header&text=kazah-png&fontSize=52&fontColor=e6edf3&animation=fadeIn&fontAlignY=55" />
</div>

<div align="center">
  <strong>Python · Rust · Go · Game automation · Computer vision · Systems engineering</strong>
  <br/><br/>
  <a href="https://github.com/kazah-png?tab=repositories">
    <img src="https://img.shields.io/badge/repositories-view%20all-0d1117?style=flat&logo=github&logoColor=white" />
  </a>
  <img src="https://komarev.com/ghpvc/?username=kazah-png&style=flat&color=161b22&label=profile+views" />
</div>

---

## About

I build systems that operate at the boundary between software and hardware — from computer vision pipelines that control Android emulators over ADB in real time, to low-level storage engines and indexing algorithms implemented from scratch in Rust and Go.

My work spans three areas: **game automation** (CV-driven bots with state machines, multi-threading, and remote control), **infrastructure** (a from-scratch message broker with exactly-once semantics and a segmented WAL), and **AI search** (HNSW-based vector database in pure Rust).

---

## Tech stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-CE422B?style=flat&logo=rust&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)

**Computer vision & AI inference**

![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![ONNX Runtime](https://img.shields.io/badge/ONNX%20Runtime-005CED?style=flat&logo=onnx&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)

ONNX execution providers: **CUDA · DirectML · TensorRT · OpenVINO · CPU** — selected at runtime.

**Mobile / emulator control**

![ADB](https://img.shields.io/badge/ADB-3DDC84?style=flat&logo=android&logoColor=white)

Full ADB pipeline over TCP. Screencap via `adb exec-out`, joystick via async `adb shell input swipe`, taps with joy-pause to preserve movement angle.

**Storage & messaging**

![LevelDB](https://img.shields.io/badge/LevelDB-4285F4?style=flat&logo=google&logoColor=white)
![bincode](https://img.shields.io/badge/bincode-CE422B?style=flat&logo=rust&logoColor=white)

**Desktop GUI & remote control**

![CustomTkinter](https://img.shields.io/badge/CustomTkinter-1f6aa5?style=flat&logo=python&logoColor=white)
![Discord](https://img.shields.io/badge/Discord%20bot-5865F2?style=flat&logo=discord&logoColor=white)
![Telegram](https://img.shields.io/badge/Telegram%20bot-2CA5E0?style=flat&logo=telegram&logoColor=white)

**Packaging & infrastructure**

![PyInstaller](https://img.shields.io/badge/PyInstaller-3776AB?style=flat&logo=python&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Actix-web](https://img.shields.io/badge/Actix--web-CE422B?style=flat&logo=rust&logoColor=white)

**Algorithms**

A\* pathfinding · HNSW approximate nearest neighbor · Priority state machine · Segmented WAL with binary index · Idempotent producer protocol

---

## Projects

### [vector-db-hnsw](https://github.com/kazah-png/vector-db-hnsw) — Vector database in Rust

Approximate nearest neighbor search engine built from scratch in Rust. Implements the **HNSW algorithm** (Hierarchical Navigable Small World) with cosine similarity, thread-safe concurrent access via `parking_lot`, persistent storage via `bincode`, and a REST API backed by Actix-web.

**Performance:** ~15 000 inserts/sec · ~5 000 queries/sec at k=10 over 100k vectors · >99 % recall at default settings.

![Rust](https://img.shields.io/badge/Rust-CE422B?style=flat&logo=rust&logoColor=white)
![Actix-web](https://img.shields.io/badge/Actix--web-CE422B?style=flat&logo=rust&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

---

### [Event-Engine](https://github.com/kazah-png/Event-Engine-Exactly-Once-Message-Broker) — Message broker in Go

Persistent message broker written from scratch in Go implementing **exactly-once delivery semantics** on the producer side. Data is stored in a segmented write-ahead log with binary indexes for O(log N) offset lookup. Consumer groups persist their progress in LevelDB.

**Performance:** 125k produce ops/s · 890k sequential fetch records/s · 42k random-offset reads/s.

Core mechanics mirror Kafka/Pulsar: rotating segments, idempotent producer registry `(producerID, sequenceNumber)`, and a commit-log consumer model.

![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![LevelDB](https://img.shields.io/badge/LevelDB-4285F4?style=flat&logo=google&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

---

### [KZH AI](https://github.com/kazah-png/kzh-ai-bot) — Brawl Stars automation bot in Python

Closed Brawl Stars farming bot built from scratch in Python. Operates entirely over ADB: captures emulator frames, runs an ONNX detector (CUDA/DirectML/TensorRT/OpenVINO), classifies game state through a priority-ordered state machine, and issues ADB commands — all inside a multi-threaded process with a CustomTkinter dashboard and optional Discord/Telegram remote control.

**Results:** ~57 % first-place rate in Trio Showdown · pushed multiple brawlers from 0 to 1 000 trophies unattended.

23-module codebase: `detect` · `state_finder` · `adaptive_brain` · `pathfinding` · `stage_manager` · `multi_worker` · `trophy_observer` · `discord_control` · `telegram_control` · `license` · `keygen_bot` · …

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![ONNX](https://img.shields.io/badge/ONNX%20Runtime-005CED?style=flat&logo=onnx&logoColor=white)
![ADB](https://img.shields.io/badge/ADB-3DDC84?style=flat&logo=android&logoColor=white)

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
