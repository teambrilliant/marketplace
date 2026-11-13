# Team Brilliant Plugin Marketplace

Central registry for discovering and installing Claude Code skill plugins.

## Usage

```bash
# Add the marketplace
/plugin marketplace add teambrilliant/marketplace

# Browse available plugins
/plugin

# Install a plugin
/plugin install tap@teambrilliant-marketplace
```

### Mods (Claude Code only)

```bash
/plugin install tap-pane@teambrilliant-marketplace
/plugin install together@teambrilliant-marketplace
```

Panes are function-hook plugins. They live in [tap](https://github.com/teambrilliant/tap) under `plugins/`, next to the skills. Every tap plugin is listed with a `"source": "git-subdir"` entry, so an install fetches only that plugin's folder.

### Codex (CLI + Mac app)

```bash
codex plugin marketplace add teambrilliant/marketplace
codex plugin add tap@teambrilliant-marketplace

# Pull latest
codex plugin marketplace upgrade teambrilliant-marketplace
```

Plugin sources use `"source": "url"` or `"git-subdir"` — Codex doesn't support Claude's `"github"` shorthand; these work in both.

## Available Plugins

| Plugin       | Description                                                             |
| ------------ | ----------------------------------------------------------------------- |
| `tap`        | Core skills: product thinking, shaping, planning, execution, QA, blast radius, repo audit |
| `tap-labs`   | Experimental skills, kept out of core until they earn a place |
| `tap-pane`   | Pane: plan progress + pinned ★ views (Claude Code only, early-access API) |
| `together`   | Shared checklists in `tap/lists` with a side pane (Claude Code only, early-access API) |

Still listed until existing installs have moved, and replaced by the plugins above: `dev-skills`, `tap-skills`, `thoughts`.

## Adding a Plugin

Add an entry to `.claude-plugin/marketplace.json` with `name`, `description`, `source`, and `version`, then push.

## Team-Wide Auto-Install

Drop config into a client repo's `.claude/settings.json` to pre-enable specific plugins — new team members get the right skills automatically.
