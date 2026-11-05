# Zankros

## 🧠 AI-Powered TUI Coding Agent

**kerf** - A fast, terminal-based coding agent built with Guile Scheme 3.x, designed to be the ultimate terminal coding companion.

![kerf](https://capsule-render.vercel.app/api?type=waving&color=0:111111,100:444444&height=180&section=header&text=kerf&fontSize=60&fontColor=ffffff&animation=fadeIn&fontAlignY=35)

---

## ✨ Features

- **🤖 Local Model Support**: Qwen, granite, and other Ollama models with native tool call support
- **⚡ Zero Build Step**: Entirely in Guile Scheme - install with `make install` or the one-line installer
- **🔧 OpenCode-Style Tools**: `bash`, `read`, `write`, `edit`, `list`, `grep`, `glob`, `patch`, `webfetch`, `todowrite`, `todoread`
- **👁️ Server Profiles**: Connect, import, test, and manage local/remote Ollama servers
- **🎯 Model Picker**: Fetch and select from available models before starting sessions
- **💬 Thinking Tokens**: Reasoning displayed as grey `∿` blocks in the transcript
- **🔄 Cancellation**: `Ctrl+C` while busy cancels in-flight requests
- **🎨 Beautiful TUI**: ANSI-styled terminal interface with spinner, status line, and interactive prompts
- **📁 Git Integration**: Full file inspection and editing capabilities
- **⚙️ Extensive Settings**: Model, workdir, timeout, temperature, tool mode, and more

---

## 🚀 Quick Start

```bash
# Install with curl
curl -sSf https://raw.githubusercontent.com/zankros/kerf/main/install.sh | sh

# Or build from source
git clone https://github.com/zankros/kerf.git
cd kerf
make install PREFIX=$HOME/.local

# Launch
kerf

# Quick connect to local Ollama
kerf --connect 192.168.68.52:11434

# Run one prompt without TUI
kerf --once "Write a Python function to sort a list"
```

---

## 🛠️ Configuration

Configuration is stored at `~/.config/kerf/config.json`:

```json
{
  "base_url": "http://192.168.68.52:11434/v1",
  "model": "qwen2.5:1.5b",
  "api_key_env": "KERF_API_KEY",
  "api_key": "",
  "workdir": "/home/keru/Projects",
  "auto_approve": false,
  "max_steps": 16,
  "timeout": 300,
  "temperature": 0.2,
  "tool_mode": "auto",
  "theme": "kerf",
  "servers": [
    {
      "name": "192.168.68.52:11434",
      "host": "192.168.68.52",
      "port": "11434",
      "scheme": "http",
      "path": "/v1",
      "model": "qwen2.5:1.5b"
    }
  ],
  "active_server": "192.168.68.52:11434"
}
```

Keybinds:
- `Ctrl+N` - Quick connect
- `Ctrl+O` - Server manager
- `Ctrl+S` - Options
- `Ctrl+P` - Command palette
- `Esc` - Back/cancel
- `Enter` - Send/action
- `q` - Quit (or insert 'q' in prompt mode)

---

## 📦 Installation

### One-Line Installer
```bash
curl -sSf https://raw.githubusercontent.com/zankros/kerf/main/install.sh | sh
```

### From Source
```bash
git clone https://github.com/zankros/kerf.git
cd kerf
make install PREFIX=$HOME/.local
```

### Verify Installation
```bash
kerf --version
# kerf 0.2.0
```

---

## 🌐 Connecting Servers

### From Windows Drive
```bash
# Connect to Ollama on Windows machine at 192.168.68.52
kerf --connect 192.168.68.52:11434
```

### Manual Server Addition
Use the Options tab → Add server, or press `Ctrl+O` then `a` to add a new server profile.

### Import from JSON
```bash
kerf --import /path/to/opencode.json
```

---

## 📸 Screenshots

| Start Page | Chat with Thinking |
|------------|-------------------|
| ![start](https://raw.githubusercontent.com/zankros/kerf/main/screenshots/start.png) | ![chat](https://raw.githubusercontent.com/zankros/kerf/main/screenshots/chat.png) |

| Model Picker | Server Manager |
|-------------|---------------|
| ![models](https://raw.githubusercontent.com/zankros/kerf/main/screenshots/models.png) | ![servers](https://raw.githubusercontent.com/zankros/kerf/main/screenshots/servers.png) |

---

## 🔐 API Key Support

- `KERF_API_KEY` environment variable
- `OPENAI_API_KEY` fallback
- `api_key` field in per-server config
- Masked display in Options tab

---

## 🛠️ Available Tools

| Tool | Description |
|------|-------------|
| `bash` | Run shell commands |
| `read` | Read file contents |
| `write` | Write to files |
| `edit` | Edit file contents |
| `list` | List directory |
| `grep` | Search file contents |
| `glob` | Find files by pattern |
| `patch` | Apply patches |
| `webfetch` | Fetch HTTP URLs |
| `todowrite` | Add todo items |
| `todoread` | Read todo items |

---

## 📄 License

[GPL-3.0](https://github.com/zankros/kerf/blob/main/LICENSE)

---

## 📬 Contact

- **GitHub**: [@zankros](https://github.com/zankros)
- **Profile**: [https://github.com/zankros/Zankros](https://github.com/zankros/Zankros)
- **Project**: [https://github.com/zankros/kerf](https://github.com/zankros/kerf)

---

*Built with Guile Scheme 3.x · No build step · Entirely source-available*