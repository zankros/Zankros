# Zankros

## About Me

I'm Keru, a creator who builds tools for the terminal. I've always been drawn to software that feels sharp, fast, and close to the metal — things that let you work directly with your system rather than abstract away from it.

### What I'm building

**kerf** — a fast TUI coding agent in Guile Scheme 3.x. It's been a journey of stripping away everything unnecessary until only the essentials remain: a terminal, a REPL, and a set of tools that get out of your way and let you code.

### Why Guile Scheme?

I wanted something with no build step, no compiled layers between me and the terminal. Pure Scheme means I can read the source, modify it, and understand every piece. It's been refreshing to build something from scratch in a language that feels both minimal and powerful.

### The name

**kerf** — a "kerf" is the gap made when something is cut. I wanted a name that sounded grounded, physical — not AI-generated. Something that evokes the act of making things in the terminal.

### What kerf offers

- **Zero setup**: `make install` or `curl | sh`, and you're running
- **Local models**: Qwen and other Ollama models that "just work" with native tool calls
- **OpenCode-style tools**: `bash`, `read`, `write`, `edit`, `list`, `grep`, `glob`, `patch`, `webfetch`, `todowrite`, `todoread`
- **Server profiles**: Quick connect, import from JSON, test connections, manage saved servers
- **Model picker**: Fetch available models before starting a session
- **Thinking tokens**: Reasoning displayed as grey `∿` blocks so you can follow the agent's thought process
- **Cancellation**: Ctrl+C while a tool runs cancels it gracefully
- **Beautiful TUI**: ANSI-styled with spinner, status line, and interactive prompts

### Getting started

```bash
# Install
curl -sSf https://raw.githubusercontent.com/zankros/kerf/main/install.sh | sh

# Launch
kerf

# Quick connect to a local Ollama instance
kerf --connect HOST:PORT

# Run one prompt without the TUI
kerf --once "Write a Python function"
```

### My setup

I run kerf from my personal workstation, connecting to local models. The project lives at `/home/keru/Projects/kerf` and is installed to `~/.local/bin/kerf`.

### Let's connect

- **GitHub**: @zankros
- **Project**: [zankros/kerf](https://github.com/zankros/kerf)
- **Profile**: [zankros/Zankros](https://github.com/zankros/Zankros)

---

*Built with Guile Scheme 3.x · No build step · Entirely source-available · MIT license not used (GPL-3.0 chosen intentionally)*

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:111111,100:444444&height=100&section=footer" alt="footer" />
</div>