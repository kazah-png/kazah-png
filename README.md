<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:21262d&height=140&section=header&text=kazah-png&fontSize=52&fontColor=e6edf3&animation=fadeIn&fontAlignY=55" />
</div>

<div align="center">
  <strong>Python · Rust · Go · C++ · C# · Java · TypeScript · Elixir</strong>
  <br/><br/>
  <a href="https://github.com/kazah-png?tab=repositories">
    <img src="https://img.shields.io/badge/repositories-view%20all-0d1117?style=flat&logo=github&logoColor=white" />
  </a>
  <img src="https://komarev.com/ghpvc/?username=kazah-png&style=flat&color=161b22&label=profile+views" />
</div>

---

## About

I build systems across several layers of the stack — game automation pipelines driven by computer vision, distributed infrastructure components implemented from scratch, real-time networking servers, and low-level Linux container primitives.

The common thread is going to the root: implementing the algorithm or the protocol directly rather than wrapping a library that already does it.

---

## Tech stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-CE422B?style=flat&logo=rust&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B17-00599C?style=flat&logo=cplusplus&logoColor=white)
![C#](https://img.shields.io/badge/C%23-.NET%208-512BD4?style=flat&logo=dotnet&logoColor=white)
![Java](https://img.shields.io/badge/Java-17-ED8B00?style=flat&logo=openjdk&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Elixir](https://img.shields.io/badge/Elixir-4B275F?style=flat&logo=elixir&logoColor=white)

**Inference & vision**

![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![ONNX Runtime](https://img.shields.io/badge/ONNX%20Runtime-005CED?style=flat&logo=onnx&logoColor=white)

ONNX execution providers: **CUDA · DirectML · TensorRT · OpenVINO · CPU**

**Storage**

![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white)
![LevelDB](https://img.shields.io/badge/LevelDB-4285F4?style=flat&logo=google&logoColor=white)
![bincode](https://img.shields.io/badge/bincode-CE422B?style=flat&logo=rust&logoColor=white)

**Networking & transport**

![ADB](https://img.shields.io/badge/ADB-3DDC84?style=flat&logo=android&logoColor=white)
![SignalR](https://img.shields.io/badge/SignalR-512BD4?style=flat&logo=dotnet&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket-3178C6?style=flat)
![Actix-web](https://img.shields.io/badge/Actix--web-CE422B?style=flat&logo=rust&logoColor=white)
![Boost.Asio](https://img.shields.io/badge/Boost.Asio-00599C?style=flat)
![GenStage](https://img.shields.io/badge/GenStage-4B275F?style=flat)

**Tooling**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![PyInstaller](https://img.shields.io/badge/PyInstaller-3776AB?style=flat&logo=python&logoColor=white)

**Algorithms**

HNSW · A\* pathfinding · Consistent hashing · Gossip protocol · CRDT (RGA) · Segmented WAL · Idempotent producer protocol · Priority state machine · Binpacking scheduler

---

## Projects

### Systems & Infrastructure

---

**[Event-Engine](https://github.com/kazah-png/Event-Engine-Exactly-Once-Message-Broker)** · Go

Persistent message broker with exactly-once producer semantics. Segmented write-ahead log with binary indexes for O(log N) offset lookup. Idempotent producer registry via `(producerID, sequenceNumber)` pairs. LevelDB consumer offset store. HTTP API.

`125k produce ops/s · 890k sequential fetch records/s · 42k random-offset reads/s`

![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![LevelDB](https://img.shields.io/badge/LevelDB-4285F4?style=flat)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

---

**[distributed-task-queue](https://github.com/kazah-png/distributed-task-queue-cpp)** · C++17

Fault-tolerant master-worker task queue. Workers register with a declared capacity and send heartbeats every 10s; the master reassigns any task from a worker that misses 3 intervals. Least-loaded worker selection. SQLite persistence. Docker Compose scale-out.

![C++](https://img.shields.io/badge/C%2B%2B17-00599C?style=flat&logo=cplusplus&logoColor=white)
![Boost.Asio](https://img.shields.io/badge/Boost.Asio-00599C?style=flat)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

---

**[mini-orchestrator](https://github.com/kazah-png/mini-orchestrator)** · Go

Container orchestrator using Linux kernel primitives directly. `unshare` + `pivot_root` for namespace isolation, cgroups v1 for CPU/memory limits, veth pairs with a bridge network and NAT for outbound connectivity, IPAM from a managed subnet. REST API for full container lifecycle. No Docker daemon or containerd involved.

![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)

---

**[distributed-kv-store](https://github.com/kazah-png/Add-distributed-KV-store-with-consistent-hashing-gossip-and-replication)** · Java

Dynamo-style key-value store. Consistent hash ring with virtual nodes for data partitioning. Gossip protocol over UDP for membership and failure detection. Replication factor 2. Transparent HTTP redirect when a request arrives at the wrong node. Docker Compose 3-node cluster.

![Java](https://img.shields.io/badge/Java-17-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

---

### AI & Search

---

**[vector-db-hnsw](https://github.com/kazah-png/vector-db-hnsw)** · Rust

Approximate nearest neighbor search engine. HNSW algorithm from scratch with cosine similarity. Thread-safe via `parking_lot::RwLock`. Persistent index via `bincode`. Actix-web REST API.

`~15k inserts/sec · ~5k queries/sec at k=10 over 100k vectors · >99% recall`

![Rust](https://img.shields.io/badge/Rust-CE422B?style=flat&logo=rust&logoColor=white)
![Actix-web](https://img.shields.io/badge/Actix--web-CE422B?style=flat&logo=rust&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

---

**[fraud-rules-engine](https://github.com/kazah-png/fraud_rules_engine)** · Elixir

Streaming event processor with declarative fraud rules. GenStage pipeline with backpressure. Sliding window counters per `(key, rule_id)` in ETS with automatic TTL expiry. Rules managed at runtime via REST API — no restart needed. Webhook alert dispatch.

![Elixir](https://img.shields.io/badge/Elixir-4B275F?style=flat&logo=elixir&logoColor=white)
![GenStage](https://img.shields.io/badge/GenStage-4B275F?style=flat)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

---

### Real-time & Networking

---

**[multiplayer-game-server](https://github.com/kazah-png/multiplayer-game-server-csharp)** · C# / .NET 8

Real-time multiplayer game server. One `GameLoopActor` per match — isolated async loop, 10 ticks/sec, no shared mutable state between rooms. SignalR WebSockets. Automatic matchmaking queue (4 players per room). Move, Attack, and Heal actions processed per tick.

![C#](https://img.shields.io/badge/C%23-.NET%208-512BD4?style=flat&logo=dotnet&logoColor=white)
![SignalR](https://img.shields.io/badge/SignalR-512BD4?style=flat&logo=dotnet&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

---

**[crdt-collaborative-editor](https://github.com/kazah-png/crdt-collaborative-editor)** · TypeScript

Real-time collaborative text editor using the RGA (Replicated Growable Array) CRDT. Operations are commutative and idempotent — no central serialization, no Operational Transform. WebSocket broadcast. Multiple clients converge to the same document state regardless of operation arrival order.

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket-3178C6?style=flat)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

---

### Automation

---

**[KZH AI](https://github.com/kazah-png/kzh-ai-bot)** · Python

Brawl Stars Trio Showdown automation bot. Operates exclusively over ADB: captures emulator frames, runs ONNX entity detection (CUDA/DirectML/TensorRT/OpenVINO), classifies game state through an 11-state priority machine, and issues ADB commands. A\* pathfinding, analog joystick emulation, fog avoidance, adaptive brain. 23-module codebase, CustomTkinter GUI, Discord/Telegram remote control, PyInstaller distribution.

`~57% first-place rate · multiple brawlers pushed 0 → 1000 trophies unattended`

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![ONNX](https://img.shields.io/badge/ONNX%20Runtime-005CED?style=flat)
![ADB](https://img.shields.io/badge/ADB-3DDC84?style=flat&logo=android&logoColor=white)

---

**[GARGUEL](https://github.com/kazah-png/GARGUEL)** · Python

Automated click-bot for Steam games. Full match cycle (~50s) with difficulty selection, auto-mode activation, and result navigation. CustomTkinter GUI with session stats and activity log. SQLite session tracking. PyInstaller standalone `.exe`.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![CustomTkinter](https://img.shields.io/badge/CustomTkinter-1f6aa5?style=flat)

---

## GitHub stats

<div align="center">
  <img height="160" src="https://github-readme-stats.vercel.app/api?username=kazah-png&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=e6edf3&text_color=8b949e&icon_color=3fb950&count_private=true" />
  <img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=kazah-png&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=e6edf3&text_color=8b949e&layout=compact&langs_count=8" />
</div>

<div align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=kazah-png&theme=github-compact&bg_color=0d1117&color=8b949e&line=3fb950&point=3fb950&hide_border=true" />
</div>

---

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:21262d,50:161b22,100:0d1117&height=80&section=footer" />
</div>
