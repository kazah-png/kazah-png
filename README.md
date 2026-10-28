# kazah-png

**Systems programming · Operating systems · Native desktop tools**

I build operating systems and native applications, from kernels and networking stacks to Windows automation tools. My main focus is C, C++, and low-level development.

## NyxOS

My main project, [NyxOS](https://github.com/nyxos-dev/nyx-os), is an x86_64 operating system built in C and Assembly. It includes a graphical desktop, TCP/IP networking, a POSIX-style userspace, and support for QEMU and physical UEFI hardware. Development and companion projects live under [nyxos-dev](https://github.com/nyxos-dev).

- **Kernel & userspace:** virtual memory, SMP, preemptive scheduling, ELF64 programs, and an EXT2 filesystem.
- **Toolchain:** a self-hosting C compiler based on TinyCC, the `xbm` package manager, and **N**, a native language that compiles to C. **N++**, its typed superset, is in design.
- **Language family:** the C implementation and 17 sibling ports, all booting, under [nyxos-dev](https://github.com/nyxos-dev).

<details>
<summary>Explore the NyxOS ecosystem</summary>

**Language implementations**

[C](https://github.com/nyxos-dev/nyx-os) · [Assembly](https://github.com/nyxos-dev/NyxOS-Asm) · [C++](https://github.com/nyxos-dev/NyxOS-Cpp) · [Rust](https://github.com/nyxos-dev/NyxOS-Rust) · [Zig](https://github.com/nyxos-dev/NyxOS-Zig) · [D](https://github.com/nyxos-dev/NyxOS-D) · [Nim](https://github.com/nyxos-dev/NyxOS-Nim) · [Ada](https://github.com/nyxos-dev/NyxOS-Ada) · [Odin](https://github.com/nyxos-dev/NyxOS-Odin) · [C#](https://github.com/nyxos-dev/NyxOS-CSharp) · [Hare](https://github.com/nyxos-dev/NyxOS-Hare) · [Go](https://github.com/nyxos-dev/NyxOS-Go) · [Swift](https://github.com/nyxos-dev/NyxOS-Swift) · [OCaml](https://github.com/nyxos-dev/NyxOS-OCaml) · [Haskell](https://github.com/nyxos-dev/NyxOS-Haskell) · [Common Lisp](https://github.com/nyxos-dev/NyxOS-Lisp) · [Pascal](https://github.com/nyxos-dev/NyxOS-Pascal) · [COBOL](https://github.com/nyxos-dev/NyxOS-COBOL)

**Desktop & tools**

- [Hemera](https://github.com/nyxos-dev/hemera) — desktop compositor.
- [Erebus](https://github.com/nyxos-dev/erebus) — terminal hosting the `nyxsh` shell.
- [Selene](https://github.com/nyxos-dev/selene) — web browser with HTTP/HTTPS support.
- [Mnemosyne](https://github.com/nyxos-dev/mnemosyne) — text editor.
- [Oneiros](https://github.com/nyxos-dev/oneiros) — generative neural network running inside NyxOS.
- [Ports](https://github.com/nyxos-dev/ports) — packages compiled inside the OS with `cc`.

</details>

## Zzen Automation

My native C++ Windows tools live under [Zzen Automation](https://github.com/zzen-automation). They automate repetitive gameplay tasks through screen recognition and standard keyboard and mouse input.

| Project | Focus | Download |
| --- | --- | --- |
| [Zzen](https://github.com/zzen-automation/Zzen) | Chronicle match automation for Inazuma Eleven: Victory Road. | [Latest release](https://github.com/zzen-automation/Zzen/releases/latest) |
| [R-Zzen](https://github.com/zzen-automation/R-Zzen) | Construction, prestige, and keep-active automation for Roblox Army Commander Tycoon. | [Latest release](https://github.com/zzen-automation/R-Zzen/releases/latest) |

---

[NyxOS website](https://nyxos.cc) · [NyxOS repositories](https://github.com/orgs/nyxos-dev/repositories) · [Zzen repositories](https://github.com/orgs/zzen-automation/repositories)
