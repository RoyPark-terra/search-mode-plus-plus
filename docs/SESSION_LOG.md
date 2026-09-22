# Search Mode ++ session log

Last updated: 2026-09-22 KST

## Durable conversation backup

The full Codex conversation is preserved separately in this immutable share link:

https://chatgpt.com/s/cx_6ab26a484ebc8191a1a81f701c669b55

The link is public to anyone who has it. Do not place passwords, API keys, cookies, or other sensitive information in this conversation.

## User requirements captured

- Connect the Search Mode ++ MCP endpoint to Codex.
- Keep the configuration durable on a PC방 computer where the local disk may reset.
- Preserve the public prompt/skill source in a separate local package and GitHub backup.
- Verify whether the plugin still works if the original Worker endpoint disappears.
- Use a local-first fallback so the prompt and core workflow remain available without the Worker.
- Preserve the conversation context so the work can be recovered after a machine reset.

## Build status

- Plugin: `search-mode-plus-plus` v0.2.0
- Local Git commit: `3f544f1`
- GitHub repository: https://github.com/RoyPark-terra/search-mode-plus-plus
- GitHub ZIP commit: `6ad71ba`
- GitHub ZIP file: `search-mode-plus-plus.zip`
- Official plugin validation: passed
- Local consistency check: passed
- MCP initialize/tools/resources check: passed at build time

## Recovery procedure

1. Download `search-mode-plus-plus.zip` from the GitHub repository.
2. Extract the archive into a persistent folder.
3. Install or open the plugin from that folder.
4. If the MCP endpoint is unavailable, keep using the packaged `skills/searchmode/SKILL.md` fallback.
5. Use this log and the Codex share link to restore the project context.

## Important boundary

The local package preserves the public prompt and skill artifacts, not the private implementation of the Cloudflare Worker. If the Worker disappears, only its server-specific MCP tools are lost; the local Search Mode workflow remains available through the packaged skill and Codex host tools.
