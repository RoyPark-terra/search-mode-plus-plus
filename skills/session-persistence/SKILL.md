---
name: session-persistence
description: Preserve Search Mode ++ project context across PC resets by reading and updating the plugin-local session log without storing secrets.
---

# Session persistence

Use `docs/SESSION_LOG.md` as the durable recovery record for this plugin.

- At the beginning of a resumed Search Mode ++ task, read the session log before making assumptions about the previous build or connection state.
- After a material change, record the current version, local/GitHub commit, verification result, recovery step, and any unresolved blocker in the session log.
- Keep the log focused on decisions and recoverable state; it is not a silent full-transcript recorder.
- Never write passwords, API keys, OAuth tokens, cookies, OTPs, private identifiers, or other secrets to the plugin, GitHub, or the session log.
- If a full conversation must be preserved, use the host’s approved conversation-export/share mechanism and record only its location and privacy warning in the log.
- Treat the remote MCP endpoint as optional. A missing Worker must not erase or invalidate the local prompt/skill fallback.
