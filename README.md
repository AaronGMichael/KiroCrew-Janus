# KiroCrew Janus

Named after the two-faced Roman god of doorways and transitions — one face toward VSCode, one toward your [KiroCrew](https://github.com/kirodotdev/KiroCrew) workspace. Run the KiroCrew dashboard inside your VSCode sidebar, with per-workspace chat scoping and editor context-menu commands. Similar to how Claude Code or Cursor bind a chat to your project — but for KiroCrew.

> **Source release in progress.** This repository currently hosts the project's issue tracker, releases, and documentation. The full source (with history) lands here soon.

## What it does

- **Sidebar dashboard.** An activity-bar view renders the KiroCrew dashboard as a live iframe. No separate window, no browser tab.
- **Per-workspace chat, automatically.** The first time you open a workspace, the extension creates a KiroCrew chat filed under a sidebar folder named after the workspace and scoped to its path.
- **Auto-authentication.** Tokens are minted against your local KiroCrew gateway automatically — no login gate, and sessions self-heal even when other KiroCrew surfaces rotate credentials.
- **Fast.** Startup mints tokens over loopback HTTP (no CLI spawn), and a stable proxy origin keeps the dashboard's asset cache warm across window reloads.
- **Editor context commands.** Right-click to seed a chat about the current file, the current selection, or every open tab.

## Requirements

- A running KiroCrew gateway on `http://localhost:5476` (default). See [KiroCrew's install docs](https://github.com/kirodotdev/KiroCrew).
- VSCode 1.85 or newer. Remote-SSH works out of the box.

## Install

From the VSCode Marketplace (search "KiroCrew Janus"), or grab the `.vsix` from [Releases](../../releases) and run:

```
code --install-extension kirocrew-janus-<version>.vsix
```

## Reporting issues

Please use the issue templates. For anything involving the dashboard not loading or auth problems, include the **KiroCrew output channel** log (View → Output → KiroCrew) — it is designed to be pasteable: tokens and cookie values are never logged, only names and fingerprints.

## License

MIT
