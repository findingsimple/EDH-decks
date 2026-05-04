# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This repository contains Magic: The Gathering EDH (Commander) decklists for a family's collection. Each deck is stored as a Markdown file in the root directory. Decks in the `wip/` directory are works in progress and may be incomplete or not yet finalized.

## Deck File Format

Each deck file (`*.md`) follows this structure:

```markdown
# Deck Name

## Commander
- Card Name

## Planeswalkers (count)
- Card Name
- Card Name

## Creatures (count)
- Card Name
- Card Name

## Sorceries (count)
## Instants (count)
## Artifacts (count)
## Enchantments (count)

## Lands (count)
- Named Land
- Named Land
- Basic Land xN

## Notes (optional)
Strategy notes, upgrade ideas, etc.
```

**Format rules:**
- One card per line, using bullet points (`- Card Name`)
- Section headers include card counts in parentheses
- Basic lands use `Basic Land xN` format (e.g., `Swamp x12`)
- Proxy cards are indicated with `(Proxy)` after the card name (e.g., `- Craterhoof Behemoth (Proxy)`)
- Optional `## Notes` section for strategy/upgrade ideas

## Lands Tracking

Real (non-proxy) land ownership is tracked centrally in `lands.md`. Always update it alongside any deck change that affects a real land:

- **Moving a real land between decks**: update `lands.md` AND both deck files in the same commit.
- **Acquiring a new real land**: add to `lands.md` and to the destination deck file (or to the "Loose Collection" section if not yet slotted).
- **Replacing a real with a proxy in a deck**: mark the deck-file entry `(Proxy)` and update `lands.md`'s `In Deck` column.
- **Conflict resolution**: if `lands.md` shows the same real card in two decks, that's a duplicate-ownership flag — investigate which copy is real and mark the other as `(Proxy)` in its deck file.

Conventions:
- `(Proxy)` after a card name in a deck file = proxy (not owned).
- Unmarked land in a deck file = owned (real).
- `lands.md` is the source of truth for "which real lands do I own and where do they live?"

## Remember

If you can't find a card or are not certain about any of the details - ask. Do not make assumptions about any details.

## Card Information

Use the scryfall-local MCP server for looking up card information, finding cards by criteria, checking card legality, or any MTG-related queries.

Key search syntax examples:
- `c:blue t:instant cmc<=2` - Blue instants with mana value 2 or less
- `t:creature pow>=5` - Creatures with power 5+
- `o:flying` - Cards with flying in oracle text
- `f:commander` - Commander-legal cards
