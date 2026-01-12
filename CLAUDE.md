# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This repository contains Magic: The Gathering EDH (Commander) decklists for a family's collection. Each deck is stored as a Markdown file.

## Deck File Format

Each deck file (`*.md`) follows this structure:

```markdown
# Deck Name

## Commander (1)
* [Card Name](cardkingdom-search-url)

## Planeswalkers (count)
## Creatures (count)
## Sorceries (count)
## Instants (count)
## Artifacts (count)
## Enchantments (count)
## Lands (count)
## Tokens (count) [optional]
```

Card entries use this format:
- Full URL: `* [Card Name](https://www.cardkingdom.com/catalog/search?search=header&filter%5Bname%5D=Card+Name)`
- Empty URL (pending): `* [Card Name]()`
- Basic lands: `* Swamp ×12` or `* Mountain x 10`

## Card Information

Use the scryfall-local MCP server for looking up card information, finding cards by criteria, checking card legality, or any MTG-related queries. The server has a local cache of all MTG cards with fast search.

Key search syntax examples:
- `c:blue t:instant cmc<=2` - Blue instants with mana value 2 or less
- `t:creature pow>=5` - Creatures with power 5+
- `o:flying` - Cards with flying in oracle text
- `f:commander` - Commander-legal cards
