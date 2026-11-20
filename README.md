# kazah-png

**Systems programming · Native Windows software · Operating-system experiments**

I build native C++ applications and explore low-level systems programming. My current public work spans independent Windows desktops, visual automation tools, and the paused NyxOS operating-system ecosystem.

## RETSAR — active development

[RETSAR](https://github.com/kazah-png/RETSAR) (*Runtime Environment for Terminal Sharing and Allocation of Resources*) is an open-source C++17 project for independent, general-purpose Windows desktop workspaces on one computer.

It explores running and managing a native secondary Windows desktop with its own applications and interaction while the main desktop remains available. RETSAR currently provides a native management console, guarded child-desktop viewer actions, and verified experiments for secondary-desktop presentation and input.

It is a **development preview**, not a production multiseat replacement. Exclusive physical-device assignment, reliable recovery, broader application compatibility, and prolonged-operation validation are still in progress.

## NyxOS — development paused

[NyxOS](https://github.com/nyxos-dev/nyx-os) is an x86_64 operating-system project written in C and Assembly, with a graphical desktop, TCP/IP networking, a POSIX-style userspace, and support for QEMU and physical UEFI hardware.

Development of NyxOS and its companion projects is currently **paused**. I do not yet have the knowledge needed to continue the project rigorously at its next stage, so I am continuing to study operating systems, computer architecture, compilers, and low-level development before returning to it with a stronger foundation.

<details>
<summary>NyxOS public projects</summary>

### Core system and tooling

- [NyxOS](https://github.com/nyxos-dev/nyx-os) — the main x86_64 operating-system project.
- [Ports](https://github.com/nyxos-dev/ports) — software and package ports for NyxOS.

### Language implementations

[C](https://github.com/nyxos-dev/nyx-os) · [Assembly](https://github.com/nyxos-dev/NyxOS-Asm) · [C++](https://github.com/nyxos-dev/NyxOS-Cpp) · [Rust](https://github.com/nyxos-dev/NyxOS-Rust) · [Zig](https://github.com/nyxos-dev/NyxOS-Zig) · [D](https://github.com/nyxos-dev/NyxOS-D) · [Nim](https://github.com/nyxos-dev/NyxOS-Nim) · [Ada](https://github.com/nyxos-dev/NyxOS-Ada) · [Odin](https://github.com/nyxos-dev/NyxOS-Odin) · [C#](https://github.com/nyxos-dev/NyxOS-CSharp) · [Hare](https://github.com/nyxos-dev/NyxOS-Hare) · [Go](https://github.com/nyxos-dev/NyxOS-Go) · [Swift](https://github.com/nyxos-dev/NyxOS-Swift) · [OCaml](https://github.com/nyxos-dev/NyxOS-OCaml) · [Haskell](https://github.com/nyxos-dev/NyxOS-Haskell) · [Common Lisp](https://github.com/nyxos-dev/NyxOS-Lisp) · [Pascal](https://github.com/nyxos-dev/NyxOS-Pascal) · [COBOL](https://github.com/nyxos-dev/NyxOS-COBOL)

### Desktop applications and experiments

- [Hemera](https://github.com/nyxos-dev/hemera) — desktop compositor.
- [Erebus](https://github.com/nyxos-dev/erebus) — terminal and `nyxsh` shell host.
- [Selene](https://github.com/nyxos-dev/selene) — web-browser project.
- [Mnemosyne](https://github.com/nyxos-dev/mnemosyne) — text-editor project.
- [Oneiros](https://github.com/nyxos-dev/oneiros) — neural-network experiment for NyxOS.

</details>

## Zzen Automation

My public native Windows automation tools use on-screen recognition with standard keyboard and mouse input.

| Project | Description |
| --- | --- |
| [Zzen](https://github.com/zzen-automation/Zzen) | Free native C++ desktop app that repeats Chronicle matches in *Inazuma Eleven: Victory Road*. |
| [R-Zzen](https://github.com/zzen-automation/R-Zzen) | Native C++ desktop app for visual automation in Roblox *Army Commander Tycoon*, including construction, prestige, and anti-AFK workflows. |

---

[RETSAR](https://github.com/kazah-png/RETSAR) · [NyxOS organization](https://github.com/nyxos-dev) · [Zzen Automation organization](https://github.com/zzen-automation)
