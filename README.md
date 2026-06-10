# Configuration

SystemD configuration for Ollama service:

```sh
cat > /etc/systemd/system/ollama.service <<'EOF'
[Unit]
Description=Ollama Service
After=network-online.target

[Service]
ExecStart=/usr/local/bin/ollama serve
User=ollama
Group=ollama
Restart=always
RestartSec=3
Environment="PATH=/home/david/.local/bin:/home/david/bin:/usr/local/bin:/usr/bin"
Environment="OLLAMA_HOST=0.0.0.0:11434"
Environment="OLLAMA_CONTEXT_LENGTH=64000"

[Install]
WantedBy=default.target
EOF
```

Pull models:

```sh
ollama pull qwen3-coder:30b
ollama pull qwen3.6:35b
ollama pull translategemma:27b
```

## OpenCode

Connect to Ollama:

```sh
cat > ~/.config/opencode/opencode.jsonc <<'EOF'
{
  "$schema": "https://opencode.ai/config.json",

  "provider": {
    "Ollama": {
      "npm": "@ai-sdk/openai-compatible",
      "options": {
        "baseURL": "http://localhost:11434/v1"
      },
      "models": {
        "qwen3-coder:30b": {
          "tools": true
        },
        "qwen3.6:35b": {
          "tools": true
        },
        "translategemma:27b": {
          "tools": true
        }
      }
    }
  },
  
  "permission": {
    "edit": "ask",
    "bash": "ask",
    "webfetch": "allow"
  }
}
EOF
```

Link directories:

```sh
ln -s $(pwd)/AGENTS.md ~/.config/opencode/AGENTS.md
ln -s $(pwd)/agents ~/.config/opencode/agents
ln -s $(pwd)/skills ~/.config/opencode/skills
ln -s $(pwd)/commands ~/.config/opencode/commands
```

## ClaudeCode

Set environment variables:

```env
OLLAMA_CONTEXT_LENGTH=64000
ANTHROPIC_AUTH_TOKEN=ollama
ANTHROPIC_API_KEY=""
ANTHROPIC_BASE_URL=http://localhost:11434
```

Link files on Windows as Administrator:

```cmd
mkdir %USERPROFILE%\.claude
mklink /j %USERPROFILE%\.claude\skills C:\...\claude-config\skills
mklink /j %USERPROFILE%\.claude\agents C:\...\claude-config\agents
mklink /j %USERPROFILE%\.claude\commands C:\...\claude-config\commands
mklink %USERPROFILE%\.claude\CLAUDE.md C:\...\claude-config\AGENTS.md
```

Link files on Linux:

```sh
mkdir -p ~/.claude/
```

Start Claude:

```sh
claude --model qwen3-coder:30b
```

Install spec-kit:

```sh
uv tool install specify-cli --from git+https://github.com/github/spec-kit.git
```

## Sources

- [agents/document-reviewer.md](./agents/document-reviewer.md) copied from [kazunori279/gcp-blogs docs-reviewer.md](https://github.com/kazunori279/gcp-blogs/blob/main/.claude/agents/docs-reviewer.md)
- [skills/spec-kit](./skills/spec-kit) copied from [SpillwaveSolutions/sdd-skill](https://github.com/SpillwaveSolutions/sdd-skill)
