<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:21262d&height=140&section=header&text=kazah-png&fontSize=52&fontColor=e6edf3&animation=fadeIn&fontAlignY=55" />
</div>

<div align="center">
  <strong>Python · Rust · Go · C · C++ · C# · Java · TypeScript · Elixir · Swift · Zig · Assembly</strong>
  <br/><br/>
  <a href="https://github.com/kazah-png?tab=repositories">
    <img src="https://img.shields.io/badge/repositories-view%20all-0d1117?style=flat&logo=github&logoColor=white" />
  </a>
  <img src="https://komarev.com/ghpvc/?username=kazah-png&style=flat&color=161b22&label=profile+views" />
</div>

---

## About

I build systems from the kernel up. Distributed infrastructure, real-time networking, game automation pipelines, container runtimes, and custom x86_64 operating systems — all implemented from scratch.

The common thread is going to the root: implementing protocols and algorithms directly instead of wrapping libraries.

---

## Tech stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-CE422B?style=flat&logo=rust&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat&logo=dotnet&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Elixir](https://img.shields.io/badge/Elixir-4B275F?style=flat&logo=elixir&logoColor=white)
![Swift](https://img.shields.io/badge/Swift-F05138?style=flat&logo=swift&logoColor=white)
![Zig](https://img.shields.io/badge/Zig-F7A41D?style=flat&logo=zig&logoColor=white)
![Assembly](https://img.shields.io/badge/x86%20Assembly-6E4C13?style=flat&logo=assemblyscript&logoColor=white)
![NyxC](https://img.shields.io/badge/%F0%9F%8C%99%20NyxC-runtime-8b5cf6?style=flat)

**Inference & vision**

![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![ONNX Runtime](https://img.shields.io/badge/ONNX%20Runtime-005CED?style=flat&logo=onnx&logoColor=white)

ONNX execution providers: CUDA · DirectML · TensorRT · OpenVINO · CPU

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

**Kernel & low-level**

![x86_64](https://img.shields.io/badge/x86__64%20Long%20Mode-00599C?style=flat)
![4-Level Paging](https://img.shields.io/badge/4--Level%20Paging-4B8BBE?style=flat)
![GDT/IDT](https://img.shields.io/badge/GDT%2FIDT-007ACC?style=flat)
![ISR/IRQ](https://img.shields.io/badge/ISR%2FIRQ-3CB371?style=flat)
![APIC](https://img.shields.io/badge/APIC-FF6600?style=flat)
![Syscalls](https://img.shields.io/badge/Syscalls-00ADD8?style=flat)
![ELF](https://img.shields.io/badge/ELF%20Loader-FFD700?style=flat)

**Tooling**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![PyInstaller](https://img.shields.io/badge/PyInstaller-3776AB?style=flat&logo=python&logoColor=white)
![NASM](https://img.shields.io/badge/NASM-009A9E?style=flat)
![QEMU](https://img.shields.io/badge/QEMU-FF6600?style=flat&logo=qemu&logoColor=white)
![GCC](https://img.shields.io/badge/GCC-FFD700?style=flat&logo=gcc&logoColor=black)

**Algorithms**

HNSW · A* pathfinding · Consistent hashing · Gossip protocol · CRDT (RGA) · Segmented WAL · Idempotent producer protocol · Priority state machine · Binpacking scheduler · SHA-256

---

## Projects

### Systems & Infrastructure

**[NyxOS](https://github.com/kazah-png/nyx-os)** · C, Assembly, 🌙 Nyx C — x86_64 kernel with GUI compositor, full TCP/IP stack, ring-3 userspace, and a native language runtime. Multiboot boot → long mode → 4-level paging (higher-half, NX+SMEP) → windowed desktop with taskbar. ELF64 loader, initramfs, `fork()` with COW, 11 syscalls via `syscall`/`sysret`, ring-3 processes with isolated page tables. EXT2 read/write with auto-mount. PC speaker + Sound Blaster 16 DMA audio. Preemptive weighted scheduler, SMP, `nice`/`renice`, job control. 40+ shell commands, pipes, env vars, Tab completion, command history. Boot animation with login screen. **🌙 Nyx C**: Go/Zig-inspired typed language that transpiles to C and runs natively on NyxOS. Written entirely from scratch — no external libraries.

[![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)](https://github.com/kazah-png/nyx-os)
[![Assembly](https://img.shields.io/badge/x86%20Assembly-6E4C13?style=flat&logo=assemblyscript&logoColor=white)](https://github.com/kazah-png/nyx-os)
[![NyxC](https://img.shields.io/badge/%F0%9F%8C%99%20NyxC-runtime-8b5cf6?style=flat)](https://github.com/kazah-png/nyx-os)
[![NASM](https://img.shields.io/badge/NASM-009A9E?style=flat)](https://github.com/kazah-png/nyx-os)
[![QEMU](https://img.shields.io/badge/QEMU-FF6600?style=flat&logo=qemu&logoColor=white)](https://github.com/kazah-png/nyx-os)

**[Event-Engine](https://github.com/kazah-png/Event-Engine-Exactly-Once-Message-Broker)** · Go — Persistent message broker with exactly-once producer semantics. Segmented write-ahead log with binary indexes for O(log N) offset lookup. Idempotent producer registry via `(producerID, sequenceNumber)` pairs. LevelDB consumer offset store. HTTP API.

`125k produce ops/s · 890k sequential fetch records/s · 42k random-offset reads/s`

[![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)](https://github.com/kazah-png/Event-Engine-Exactly-Once-Message-Broker)
[![LevelDB](https://img.shields.io/badge/LevelDB-4285F4?style=flat&logo=google&logoColor=white)](https://github.com/kazah-png/Event-Engine-Exactly-Once-Message-Broker)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)](https://github.com/kazah-png/Event-Engine-Exactly-Once-Message-Broker)

**[distributed-task-queue](https://github.com/kazah-png/distributed-task-queue-cpp)** · C++17 — Fault-tolerant master-worker task queue. Workers register with declared capacity and send heartbeats every 10s; the master reassigns tasks from unresponsive workers after 3 missed intervals. Least-loaded worker selection. SQLite persistence. Docker Compose scale-out.

[![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)](https://github.com/kazah-png/distributed-task-queue-cpp)
[![Boost.Asio](https://img.shields.io/badge/Boost.Asio-00599C?style=flat)](https://github.com/kazah-png/distributed-task-queue-cpp)
[![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white)](https://github.com/kazah-png/distributed-task-queue-cpp)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)](https://github.com/kazah-png/distributed-task-queue-cpp)

**[mini-orchestrator](https://github.com/kazah-png/mini-orchestrator)** · Go — Container orchestrator built on raw Linux kernel primitives. `unshare` + `pivot_root` for namespace isolation, cgroups v1 for CPU/memory limits, veth pairs with bridge network and NAT for outbound connectivity, IPAM from a managed subnet. REST API for full container lifecycle. No Docker daemon or containerd involved.

[![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)](https://github.com/kazah-png/mini-orchestrator)
[![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)](https://github.com/kazah-png/mini-orchestrator)

**[distributed-kv-store](https://github.com/kazah-png/Add-distributed-KV-store-with-consistent-hashing-gossip-and-replication)** · Java — Dynamo-style key-value store. Consistent hash ring with virtual nodes for data partitioning. Gossip protocol over UDP for membership and failure detection. Replication factor 2. Transparent HTTP redirect on wrong-node requests. Docker Compose 3-node cluster.

[![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)](https://github.com/kazah-png/Add-distributed-KV-store-with-consistent-hashing-gossip-and-replication)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)](https://github.com/kazah-png/Add-distributed-KV-store-with-consistent-hashing-gossip-and-replication)

**[distributed-cron-scheduler](https://github.com/kazah-png/distributed-cron-scheduler-swift)** · Swift / Vapor — Fault-tolerant distributed cron scheduler. Leadership via PostgreSQL advisory lock with TTL; only the leader executes jobs, standby takes over within seconds on crash. Full run history, retry with exponential backoff, REST API, 2-node Docker Compose cluster.

[![Swift](https://img.shields.io/badge/Swift-F05138?style=flat&logo=swift&logoColor=white)](https://github.com/kazah-png/distributed-cron-scheduler-swift)
[![Vapor](https://img.shields.io/badge/Vapor-4-0099CC?style=flat)](https://github.com/kazah-png/distributed-cron-scheduler-swift)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)](https://github.com/kazah-png/distributed-cron-scheduler-swift)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)](https://github.com/kazah-png/distributed-cron-scheduler-swift)

---

### AI & Search

**[vector-db-hnsw](https://github.com/kazah-png/vector-db-hnsw)** · Rust — Approximate nearest neighbor search engine. HNSW algorithm from scratch with cosine similarity. Thread-safe via `parking_lot::RwLock`. Persistent index via `bincode`. Actix-web REST API.

`~15k inserts/sec · ~5k queries/sec at k=10 over 100k vectors · >99% recall`

[![Rust](https://img.shields.io/badge/Rust-CE422B?style=flat&logo=rust&logoColor=white)](https://github.com/kazah-png/vector-db-hnsw)
[![Actix-web](https://img.shields.io/badge/Actix--web-CE422B?style=flat&logo=rust&logoColor=white)](https://github.com/kazah-png/vector-db-hnsw)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)](https://github.com/kazah-png/vector-db-hnsw)

**[fraud-rules-engine](https://github.com/kazah-png/fraud_rules_engine)** · Elixir — Streaming event processor with declarative fraud rules. GenStage pipeline with backpressure. Sliding window counters per `(key, rule_id)` in ETS with automatic TTL expiry. Rules managed at runtime via REST API — no restart needed. Webhook alert dispatch.

[![Elixir](https://img.shields.io/badge/Elixir-4B275F?style=flat&logo=elixir&logoColor=white)](https://github.com/kazah-png/fraud_rules_engine)
[![GenStage](https://img.shields.io/badge/GenStage-4B275F?style=flat)](https://github.com/kazah-png/fraud_rules_engine)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)](https://github.com/kazah-png/fraud_rules_engine)

**[prometheus-like-tsdb](https://github.com/kazah-png/prometheus-like-tsdb-zig)** · Zig — Time series database from scratch, zero external dependencies. Gorilla XOR compression for float64 samples (~1.4 bytes/sample), DFCM timestamp encoding, write-ahead log for crash recovery, inverted label index for fast selector queries, aggregations (sum, avg, max, min), memory-mapped block files. HTTP API compatible with Prometheus text exposition format.

[![Zig](https://img.shields.io/badge/Zig-F7A41D?style=flat&logo=zig&logoColor=white)](https://github.com/kazah-png/prometheus-like-tsdb-zig)

---

### Real-time & Networking

**[multiplayer-game-server](https://github.com/kazah-png/multiplayer-game-server-csharp)** · C# / .NET 8 — Real-time multiplayer game server. One `GameLoopActor` per match — isolated async loop, 10 ticks/sec, no shared mutable state between rooms. SignalR WebSockets. Automatic matchmaking queue (4 players per room). Move, Attack, and Heal actions processed per tick.

[![C#](https://img.shields.io/badge/C%23-512BD4?style=flat&logo=dotnet&logoColor=white)](https://github.com/kazah-png/multiplayer-game-server-csharp)
[![SignalR](https://img.shields.io/badge/SignalR-512BD4?style=flat&logo=dotnet&logoColor=white)](https://github.com/kazah-png/multiplayer-game-server-csharp)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)](https://github.com/kazah-png/multiplayer-game-server-csharp)

**[crdt-collaborative-editor](https://github.com/kazah-png/crdt-collaborative-editor)** · TypeScript — Real-time collaborative text editor using the RGA (Replicated Growable Array) CRDT. Operations are commutative and idempotent — no central serialization, no Operational Transform. WebSocket broadcast. Multiple clients converge to the same document state regardless of operation arrival order.

[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)](https://github.com/kazah-png/crdt-collaborative-editor)
[![WebSocket](https://img.shields.io/badge/WebSocket-3178C6?style=flat)](https://github.com/kazah-png/crdt-collaborative-editor)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)](https://github.com/kazah-png/crdt-collaborative-editor)

---

### Automation

**[GARGUEL](https://github.com/kazah-png/GARGUEL)** · Python — Automated click-bot for Steam games. Full match cycle with difficulty selection, auto-mode activation, and result navigation. CustomTkinter GUI with session stats and activity log. SQLite session tracking. Standalone `.exe` via PyInstaller.

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)](https://github.com/kazah-png/GARGUEL)
[![CustomTkinter](https://img.shields.io/badge/CustomTkinter-1f6aa5?style=flat)](https://github.com/kazah-png/GARGUEL)

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
