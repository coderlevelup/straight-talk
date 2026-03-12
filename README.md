# Straight Talk

A Claude Code plugin that eliminates sycophancy, fluff, and hedging. Makes Claude direct, honest, and useful.

> After testing, this plugin will be published to the Kyros marketplace.

## What it does

Applies communication rules that stop Claude from:
- Opening with "Great question!" or similar filler praise
- Softening criticism with "have you considered..." instead of stating the problem
- Glossing over errors to be polite
- Guessing when it doesn't know
- Implementing against hypothetical features

And makes Claude:
- State problems directly
- Challenge assumptions and point out errors
- Suggest better alternatives proactively
- Prioritise useful feedback over comfortable feedback

## Install

### Option 1: Plugin (recommended)

Install as a Claude Code plugin to get `/straight-talk:apply` (try it) and `/straight-talk:install` (make it permanent).

```bash
# Once published to Kyros marketplace:
# /plugin marketplace add kyros
# /plugin install straight-talk@kyros

# For now, test locally:
claude --plugin-dir /path/to/straight-talk
```

### Option 2: Shell script

Writes the rules directly to `~/.claude/CLAUDE.md` (always active, no plugin needed):

```bash
curl -s https://raw.githubusercontent.com/campey/straight-talk/main/install.sh | bash
```

### Option 3: Manual

Copy the rules from `skills/apply/SKILL.md` into your `~/.claude/CLAUDE.md`.

## Skills

| Skill | Command | Description |
|-------|---------|-------------|
| apply | `/straight-talk:apply` | Apply rules to the current session only |
| install | `/straight-talk:install` | Merge rules into `~/.claude/CLAUDE.md` permanently, intelligently handling any existing overlapping rules |

## Uninstall

Remove the `# Straight Talk` section from `~/.claude/CLAUDE.md`.
