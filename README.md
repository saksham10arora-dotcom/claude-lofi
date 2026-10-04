# lofi

**A soundtrack that follows your session.** A [Claude Code](https://code.claude.com) mod.

**[▶ Watch with sound](demo/lofi.mp4)** (30 s)

The mod's own tracks, sequenced the way a session drives them.

**calm** while Claude is idle, **focus** while it works, **flow** when it's editing hard (3 edits inside a minute); a chime when a test command passes, a low note when it fails, a chord when a long turn finishes, then silence after a few idle minutes. Off until `/lofi on`.

Every sound is original, synthesised from scratch by [`scripts/make_audio.py`](scripts/make_audio.py) (Rhodes-style 9th chords, warm bass, swung drums, vinyl crackle), so there is nothing to license. Rerun it to make your own.

## Commands and settings

- `/lofi on`, `/lofi off`, `/lofi vol 0-100`, `/lofi status`
- Settings: volume (default 30), minutes of calm after a turn (default 3)

## What it touches

Its own audio files, played through the system player (`afplay` on macOS).

## Install

Claude Code **2.1.287 or newer** runs mods out of the box. On 2.1.273 to 2.1.286, start it with `CLAUDE_CODE_ENABLE_FUNCTION_HOOKS=1` first.

```bash
claude plugin marketplace add saksham10arora-dotcom/claude-lofi
claude plugin install lofi@nerfsaksham-lofi
```

Every option has a default, so the installer's "userConfig options not yet set" note is safe to ignore.

Or try it without installing:

```bash
git clone https://github.com/saksham10arora-dotcom/claude-lofi && claude --plugin-dir claude-lofi
```

## Develop

```bash
claude plugin validate .
claude plugin test .
```

## More mods

Part of a set: [teach-me](https://github.com/saksham10arora-dotcom/claude-teach-me) · [vhs](https://github.com/saksham10arora-dotcom/claude-vhs) · [frugal](https://github.com/saksham10arora-dotcom/claude-frugal) · [lofi](https://github.com/saksham10arora-dotcom/claude-lofi). More community mods: [awesome-claude-mods](https://github.com/saksham10arora-dotcom/awesome-claude-mods).

MIT. Made by [Saksham Arora](https://saksham.digital) ([@nerfsaksham](https://x.com/nerfsaksham)).
