# Search Mode ++ Codex plugin

Local-first Search Mode ++ package for Codex. The downloadable ZIP contains the validated plugin, public upstream prompt/skill snapshot, optional MCP configuration, and local fallback documentation.

## Restore after a PC reset

1. Download `search-mode-plus-plus.zip`.
2. Extract it to a persistent folder.
3. Install or open the plugin from that folder.
4. Read `docs/SESSION_LOG.md` to recover the task context.

The remote MCP endpoint is optional. If it disappears, the packaged local skill remains available; only server-specific MCP tools are lost.

- [Session recovery log](docs/SESSION_LOG.md)
- [Session persistence skill](skills/session-persistence/SKILL.md)
- [Plugin backup](search-mode-plus-plus.zip)

The session log contains a link to the preserved Codex conversation. Do not add passwords, API keys, cookies, or other secrets to this public repository.
