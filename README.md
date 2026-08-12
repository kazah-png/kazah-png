<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:21262d&height=140&section=header&text=kazah-png&fontSize=52&fontColor=e6edf3&animation=fadeIn&fontAlignY=55" />
</div>

<div align="center">
  <strong>Systems &amp; OS development — from-scratch everything</strong>
  <br/><br/>
  <sub>C · Assembly · Rust · C++ · Zig · D · Nim · Ada · Odin · C# · Hare · Go · Swift · OCaml · Haskell · Lisp · Python · TypeScript · Elixir · Java</sub>
  <br/><br/>
  <a href="https://github.com/kazah-png?tab=repositories">
    <img src="https://img.shields.io/badge/repositories-view%20all-0d1117?style=flat&logo=github&logoColor=white" />
  </a>
  <img src="https://komarev.com/ghpvc/?username=kazah-png&style=flat&color=161b22&label=profile+views" />
</div>

---

## About

I build systems from the kernel up. Distributed infrastructure, real-time networking, game automation pipelines, container runtimes, and custom x86_64 operating systems — all implemented from scratch.

The common thread is going to the root: implementing protocols and algorithms directly instead of wrapping libraries. Lately that has meant **rebuilding the same operating system from zero, one language after another** — a polyglot family that boots on bare metal in **11 languages** and counting.

---

## Languages

![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)
![Assembly](https://img.shields.io/badge/x86%20Assembly-6E4C13?style=flat&logo=assemblyscript&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-CE422B?style=flat&logo=rust&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)
![Zig](https://img.shields.io/badge/Zig-F7A41D?style=flat&logo=zig&logoColor=white)
![D](https://img.shields.io/badge/D-B03931?style=flat&logo=d&logoColor=white)
![Nim](https://img.shields.io/badge/Nim-FFE953?style=flat&logo=nim&logoColor=black)
![Ada](https://img.shields.io/badge/Ada-2E8B57?style=flat&logo=ada&logoColor=white)
![Odin](https://img.shields.io/badge/Odin-3B7FBF?style=flat&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat&logo=dotnet&logoColor=white)
![Hare](https://img.shields.io/badge/Hare-9E6B4A?style=flat&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![Swift](https://img.shields.io/badge/Swift-F05138?style=flat&logo=swift&logoColor=white)
![OCaml](https://img.shields.io/badge/OCaml-EC6813?style=flat&logo=ocaml&logoColor=white)
![Haskell](https://img.shields.io/badge/Haskell-5D4F85?style=flat&logo=haskell&logoColor=white)
![Common Lisp](https://img.shields.io/badge/Common%20Lisp-522FA0?style=flat&logo=commonlisp&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Elixir](https://img.shields.io/badge/Elixir-4B275F?style=flat&logo=elixir&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![N](https://img.shields.io/badge/%F0%9F%8C%99%20N-v0.2-8b5cf6?style=flat)
![N++](https://img.shields.io/badge/%F0%9F%8C%99%20N%2B%2B-design-8b5cf6?style=flat)

---

## Flagship — NyxOS

**[NyxOS](https://github.com/kazah-png/nyx-os)** · C, Assembly — a from-scratch x86_64 operating system. Multiboot → long mode → 4-level paging (higher-half, NX + SMEP), a double-buffered window compositor with taskbar, a full TCP/IP stack, and a ring-3 POSIX-style userspace (ELF64 loader, copy-on-write `fork`, 57 syscalls via `syscall`/`sysret`, per-process isolated page tables). EXT2 read/write with auto-mount, SMP multi-core, PC speaker + Sound Blaster 16 audio, a preemptive weighted scheduler, and 40+ shell commands. Ships an **in-OS C toolchain** — a ported TinyCC that compiles C to native ELF inside the running system and **self-hosts**: the compiler compiles its own source, then `cc --self` builds programs with that self-built compiler. Also home to **N** and **N++**, its native languages: N compiles to C through the in-OS toolchain today, and N++ is the typed superset in design — one language family built for one OS, HolyC-style. Written entirely from scratch — no external libraries.

[![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)](https://github.com/kazah-png/nyx-os)
[![Assembly](https://img.shields.io/badge/x86%20Assembly-6E4C13?style=flat&logo=assemblyscript&logoColor=white)](https://github.com/kazah-png/nyx-os)
[![N](https://img.shields.io/badge/%F0%9F%8C%99%20N-v0.2-8b5cf6?style=flat)](https://github.com/kazah-png/nyx-os/tree/master/lang)
[![N++](https://img.shields.io/badge/%F0%9F%8C%99%20N%2B%2B-design-8b5cf6?style=flat)](https://github.com/kazah-png/nyx-os/tree/master/lang)
[![NASM](https://img.shields.io/badge/NASM-009A9E?style=flat)](https://github.com/kazah-png/nyx-os)
[![QEMU](https://img.shields.io/badge/QEMU-FF6600?style=flat&logo=qemu&logoColor=white)](https://github.com/kazah-png/nyx-os)

---

## The NyxOS family — one OS, many languages

The same operating system, rebuilt from zero in a different language each time: same Multiboot → long-mode bring-up, a native toolchain per language, each verified by booting in QEMU. **11 boot to a screen today — 5 more are in progress.**

**Booting now**

[![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)](https://github.com/kazah-png/nyx-os)
[![Assembly](https://img.shields.io/badge/Assembly-6E4C13?style=flat&logo=assemblyscript&logoColor=white)](https://github.com/kazah-png/NyxOS-Asm)
[![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)](https://github.com/kazah-png/NyxOS-Cpp)
[![Rust](https://img.shields.io/badge/Rust-CE422B?style=flat&logo=rust&logoColor=white)](https://github.com/kazah-png/NyxOS-Rust)
[![Zig](https://img.shields.io/badge/Zig-F7A41D?style=flat&logo=zig&logoColor=white)](https://github.com/kazah-png/NyxOS-Zig)
[![D](https://img.shields.io/badge/D-B03931?style=flat&logo=d&logoColor=white)](https://github.com/kazah-png/NyxOS-D)
[![Nim](https://img.shields.io/badge/Nim-FFE953?style=flat&logo=nim&logoColor=black)](https://github.com/kazah-png/NyxOS-Nim)
[![Ada](https://img.shields.io/badge/Ada-2E8B57?style=flat&logo=ada&logoColor=white)](https://github.com/kazah-png/NyxOS-Ada)
[![Odin](https://img.shields.io/badge/Odin-3B7FBF?style=flat&logoColor=white)](https://github.com/kazah-png/NyxOS-Odin)
[![C#](https://img.shields.io/badge/C%23-512BD4?style=flat&logo=dotnet&logoColor=white)](https://github.com/kazah-png/NyxOS-CSharp)
[![Hare](https://img.shields.io/badge/Hare-9E6B4A?style=flat&logoColor=white)](https://github.com/kazah-png/NyxOS-Hare)

**In progress**

[![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)](https://github.com/kazah-png/NyxOS-Go)
[![Swift](https://img.shields.io/badge/Swift-F05138?style=flat&logo=swift&logoColor=white)](https://github.com/kazah-png/NyxOS-Swift)
[![OCaml](https://img.shields.io/badge/OCaml-EC6813?style=flat&logo=ocaml&logoColor=white)](https://github.com/kazah-png/NyxOS-OCaml)
[![Haskell](https://img.shields.io/badge/Haskell-5D4F85?style=flat&logo=haskell&logoColor=white)](https://github.com/kazah-png/NyxOS-Haskell)
[![Common Lisp](https://img.shields.io/badge/Common%20Lisp-522FA0?style=flat&logo=commonlisp&logoColor=white)](https://github.com/kazah-png/NyxOS-Lisp)

**Bare-metal toolchain** — Multiboot1 + GRUB, hand-written boot stubs, per-language native compilers (rustc, zig, LDC, Nim, GNAT, Odin, bflat, Hare, …), linked to a custom `linker.ld` and booted headless in QEMU.

![Multiboot](https://img.shields.io/badge/Multiboot1-4E2A8E?style=flat)
![GRUB](https://img.shields.io/badge/GRUB-2A1E5C?style=flat)
![NASM](https://img.shields.io/badge/NASM-009A9E?style=flat)
![LLVM](https://img.shields.io/badge/LLVM-262D3A?style=flat&logo=llvm&logoColor=white)
![GNU Make](https://img.shields.io/badge/GNU%20Make-A42E2B?style=flat&logo=gnu&logoColor=white)
![QEMU](https://img.shields.io/badge/QEMU-FF6600?style=flat&logo=qemu&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)

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
