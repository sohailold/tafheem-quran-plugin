# Tafheem-ul-Quran for Claude

Search and quote **Tafheem-ul-Quran** (Sayyid Abul A'la Maududi), the six major hadith collections, a library of Islamic books, the Nizamaat topics, and Islamic history — from [tafheemulquran.net](https://tafheemulquran.net), with a link to every source.

This repository is a [Claude Code](https://claude.com/claude-code) plugin. It connects Claude to the site's free, read-only MCP server and adds a `tafheem-research` skill that tells Claude how to use it well: which tools fit which question, how to cite, and how to keep Maududi's words separate from its own.

## Install (Claude Code)

```
/plugin install tafheem-quran --marketplace sohailold/tafheem-quran-plugin
```

On older Claude Code versions, add the marketplace first:

```
/plugin marketplace add sohailold/tafheem-quran-plugin
/plugin install tafheem-quran@tafheem
```

or from a terminal:

```
claude plugin marketplace add sohailold/tafheem-quran-plugin
claude plugin install tafheem-quran@tafheem
```

Then ask, for example: *"Show Tafheem-ul-Quran's translation of 2:255 with its notes."*

Only want the server, without the skill? `claude mcp add --transport http tafheem https://tafheemulquran.net/mcp`

## Claude.ai, ChatGPT and other apps

Add `https://tafheemulquran.net/mcp` as a custom connector (no sign-in, Streamable HTTP). Step-by-step guide: <https://tafheemulquran.net/mcp-guide>

## What's included

| Path | Purpose |
|---|---|
| `.claude-plugin/marketplace.json` | The `tafheem` marketplace, listing this plugin |
| `plugins/tafheem-quran/.mcp.json` | The MCP server `https://tafheemulquran.net/mcp` (15 read-only tools) |
| `plugins/tafheem-quran/skills/tafheem-research/SKILL.md` | How to research and cite with it |

## اردو

یہ Claude Code کا پلگ اِن ہے جو Claude کو tafheemulquran.net سے جوڑتا ہے: تفہیم القرآن (ترجمہ و حواشی)، صحاحِ ستہ، اسلامی کتب، نظامات اور اسلامی تاریخ — ہر حوالے کے لنک کے ساتھ۔ اوپر دی گئی دو کمانڈز سے انسٹال کریں۔ Claude.ai یا ChatGPT میں جوڑنے کا طریقہ: <https://tafheemulquran.net/mcp-guide>

## Privacy, terms, support

- Privacy policy: <https://tafheemulquran.net/privacy> (the server stores none of your questions)
- Terms of use: <https://tafheemulquran.net/terms>
- Support: tafheem2026@gmail.com

## License

The plugin files in this repository are MIT licensed. The texts served by tafheemulquran.net (Tafheem-ul-Quran, books, translations) belong to their authors and publishers and are not covered by this license — see the site's [terms](https://tafheemulquran.net/terms).
