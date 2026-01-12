# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This repository contains Magic: The Gathering EDH (Commander) decklists for a family's collection. Each deck is stored as a Markdown file.

## Deck File Format

Each deck file (`*.md`) follows this structure:

```markdown
# Deck Name

## Commander
Card Name

## Planeswalkers (count)
Card Name
Card Name

## Creatures (count)
Card Name
Card Name

## Sorceries (count)
## Instants (count)
## Artifacts (count)
## Enchantments (count)

## Lands (count)
Named Land
Named Land
Basic Land xN

## Notes (optional)
Strategy notes, upgrade ideas, etc.
```

**Format rules:**
- One card per line, no bullets or links
- Section headers include card counts in parentheses
- Basic lands use `Basic Land xN` format (e.g., `Swamp x12`)
- Optional `## Notes` section for strategy/upgrade ideas

## Card Information

Use the scryfall-local MCP server for looking up card information, finding cards by criteria, checking card legality, or any MTG-related queries.

Key search syntax examples:
- `c:blue t:instant cmc<=2` - Blue instants with mana value 2 or less
- `t:creature pow>=5` - Creatures with power 5+
- `o:flying` - Cards with flying in oracle text
- `f:commander` - Commander-legal cards
