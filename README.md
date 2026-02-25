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

## Available Plugins

| Plugin       | Description                                                             |
| ------------ | ----------------------------------------------------------------------- |
| `tap-skills` | TAP methodology — audit, QA, blast radius, system health, retrospective |
| `dev-skills` | Developer workflow skills for Claude Code                                |

## Adding a Plugin

Add an entry to `.claude-plugin/marketplace.json` with `name`, `description`, `source`, and `version`, then push.

## Team-Wide Auto-Install

Drop config into a client repo's `.claude/settings.json` to pre-enable specific plugins — new team members get the right skills automatically.
