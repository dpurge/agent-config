# Claude code with Ollama

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
mklink %USERPROFILE%\.claude\CLAUDE.md C:\...\claude-config\CLAUDE.md
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
