# Team Brilliant Plugin Marketplace

Central registry for discovering and installing Claude Code skill plugins.

## Usage

```bash
# Add the marketplace
/plugin marketplace add teambrilliant/marketplace

# Browse available plugins
/plugin

# Install a plugin
/plugin install tap-skills@teambrilliant
```

### Codex (CLI + Mac app)

```bash
codex plugin marketplace add teambrilliant/marketplace
codex plugin add dev-skills@teambrilliant-marketplace
codex plugin add tap-skills@teambrilliant-marketplace

# Pull latest
codex plugin marketplace upgrade teambrilliant-marketplace
```

Mods (function-hook plugins) live in [claude-code-mods](https://github.com/teambrilliant/claude-code-mods), one folder each, listed with `"source": "git-subdir"` — only that folder is fetched. Claude Code only.

```bash
/plugin install thoughts@teambrilliant-marketplace
```

Plugin sources use `"source": "url"` — Codex doesn't support Claude's `"github"` shorthand; `url` works in both.

## Available Plugins

| Plugin       | Description                                                             |
| ------------ | ----------------------------------------------------------------------- |
| `tap-skills` | TAP methodology — audit, QA, blast radius, system health, retrospective |
| `dev-skills` | Developer workflow skills for Claude Code                                |
| `thoughts`   | Mod: plan progress + pinned ★ views in a side pane (Claude Code only, early-access mods API) |

## Adding a Plugin

Add an entry to `.claude-plugin/marketplace.json` with `name`, `description`, `source`, and `version`, then push.

## Team-Wide Auto-Install

Drop config into a client repo's `.claude/settings.json` to pre-enable specific plugins — new team members get the right skills automatically.
