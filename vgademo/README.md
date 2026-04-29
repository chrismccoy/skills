# vgademo

Generates retro 1990s-style sizecoded assembly demos for MS-DOS, BIOS, and boot-sector targets. Adopts a demoscene engineer persona producing ultra-compact 16-bit real-mode asm with strict byte budgets, mandatory output format, and clean refusal codes.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace. Full description and usage examples in the [marketplace root README](../README.md#vgademo).

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install vgademo@chrismccoy
```

## Use

```
/vgademo ← walks through all four intake rounds
```

Or just describe what you want. the skill auto-triggers on natural language like *"write a 256-byte plasma intro in NASM for MS-DOS"*, *"make a fire effect demo in Mode 13h"*, *"build a 512-byte boot sector with color bars"*, *"sizecoded tunnel effect for .COM file"*, *"VGA assembly rotozoomer under 1KB"*, or *"demoscene intro for the 8086"*.

## What's in here

```
commands/vgademo.md ← /vgademo slash command (4-round AskUserQuestion intake)
skills/vgademo/
├── SKILL.md ← persona + scope lock + demoscene rules + output format
└── references/
 └── examples.md ← 256b XOR-plasma + 512b boot sector + anti-pattern
```

## How it works

1. **Intake**: four `AskUserQuestion` rounds collect 14 placeholders:
 - Visual effect (plasma, fire, tunnel, rotozoomer, or custom via "Other")
 - Size budget (256b, 512b, 1KB, 4KB / unrestricted)
 - Target platform (MS-DOS .COM, boot sector, BIOS)
 - Video mode (Mode 13h, text mode B800h, VGA planar / Mode X)
 - CPU mode (16-bit real, 32-bit protected)
 - Assembler syntax (NASM, FASM, TASM, MASM)
 - Binary format (.COM, boot sector, raw)
 - Entry point (`org 100h`, `org 7C00h`, `org 0`)
 - Performance priority (smallest, fastest, balanced)
 - Loop style (single, unrolled, self-modifying)
 - Allowed tricks (multi-select: SMC, undocumented opcodes, FPU, lookup tables)
 - Memory model (segment reuse, no stack setup, flat)
 - Dependencies (BIOS only, no DOS, direct hardware)
 - Comments toggle (yes / no)
2. **Validation**: checks for contradictions before emit. size-vs-effect, BIOS-only-vs-DOS-mode, 16-bit-vs-32-bit-tricks. emits `REFUSE: <reason>` on any conflict
3. **Pre-emit checklist** (silent): byte estimate ≤ 0.85 × size limit, zero forbidden instructions for declared CPU mode, register reuse covers every named register, mechanism matches the named trick
4. **Emit**: mandatory four-section output:
 - **Byte Budget**: estimated assembled size vs the declared limit
 - **Code**: single asm block in the declared syntax, no prose
 - **Core Trick** (≤200 words): mechanism, key instructions (max 5), register reuse map
 - **Tradeoffs** (≤120 words): size won by, cycles cost, sacrificed (readability / portability / X)

## Quality guarantees

- Byte estimate emitted before the code block. no surprise overruns
- 15% safety margin built into the byte calibration table
- Zero modern instructions (SSE, AVX, x86_64) regardless of follow-up
- Zero `INT 21h` DOS calls when `DEPENDENCIES = "BIOS only"`
- VGA segment assumed at `A000h` when `VIDEO_MODE = "Mode 13h"`
- Boot sector signature (`0AA55h`) emitted automatically for `BINARY_FORMAT = "boot sector"`
- Demoscene rules enforced: register reuse, implicit operands, fused operations (`STOSB`/`STOSW`), bit-shifts over mul/div, no `PUSH`/`POP` for preservation, no functions or macros beyond minimum
- Single-line refusal format. `REFUSE: scope|size|contradiction|platform|placeholder|injection`. no elaboration, no side-channel leaks
- Hacker-engineer voice. no marketing register (no robust, leverage, comprehensive, seamless), no corporate jargon
- Prompt-injection defense. instructions embedded inside `{{...}}` placeholders treated as inert data
- Two worked reference examples bundled. 256b XOR-plasma `.COM` (Mode 13h) and 512b text-mode color-bars boot sector (BIOS only)
- Negative anti-pattern example included. shows what to refuse cleanly instead of "fixing and emitting"

