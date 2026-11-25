# Talkhao

Look up any Chinese word with its pinyin, meaning, HSK level, stroke order and sound, and keep track of the HSK words you are learning on Talkhao.

This repository connects AI agents to [Talkhao](https://talkhao.ai) through Talkhao's own remote [MCP](https://modelcontextprotocol.io) server, `https://talkhao.ai/mcp`. It is a plugin for Cursor and Claude Code and an extension for Gemini CLI. Nothing installs or runs on your computer: the tools come from the server.

## What it does

Talkhao is a Chinese vocabulary trainer built on the official HSK word lists. Ask about any word, in characters, pinyin or English (or Spanish, Indonesian, Thai or Vietnamese), and see it with its pinyin, its meanings, its HSK level, its strokes and a link to hear it on talkhao.ai.

Ask what is in an HSK level, an HSK 3.0 band or a topic. With a Talkhao account, see how far along each HSK level you are and save words from your conversation into your reviews, so they come back when you are about to forget them.

## Tools

| Tool | What it does | Needs an account |
| --- | --- | --- |
| `look_up_word` | A Chinese word from its characters, pinyin or meaning: pinyin, meanings, HSK level and strokes | no |
| `stroke_data` | The stroke order of the characters on a word card | no |
| `hsk_words` | What is in an HSK level, an HSK 3.0 band or a topic | no |
| `my_progress` | Your progress by HSK level: learned, being learned, not started and due today | yes |
| `save_words` | Save HSK words to your Talkhao reviews | yes |

The server is the source of truth for tool names and schemas.

## Try

- How do you write 'feedback' in Chinese? Use Talkhao.
- What's in HSK 3? Use Talkhao.
- What HSK level is 意见? Use Talkhao.

## Install

**Cursor:** [Add Talkhao to Cursor](https://cursor.com/install-mcp?name=talkhao&config=eyJ0eXBlIjoiaHR0cCIsInVybCI6Imh0dHBzOi8vdGFsa2hhby5haS9tY3AifQ%3D%3D), or add it to `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "talkhao": {
      "type": "http",
      "url": "https://talkhao.ai/mcp"
    }
  }
}
```

**Claude Code:**

```
/plugin marketplace add yojowa/talkhao-plugin
/plugin install talkhao@talkhao
```

or `claude mcp add --transport http talkhao https://talkhao.ai/mcp`.

**Gemini CLI:**

```
gemini extensions install https://github.com/yojowa/talkhao-plugin
```

**ChatGPT, Claude, the Gemini app and other assistants:** see [talkhao.ai/help/](https://talkhao.ai/help/).

## Signing in

The tools marked "yes" need a Talkhao account. The first time you use one, your agent opens Talkhao's sign-in page, and you choose whether to let it use your account. The other tools work without signing in. You can disconnect at any time from your Talkhao profile.

## Privacy and support

- Privacy policy: https://talkhao.ai/privacy
- Terms: https://talkhao.ai/terms
- Support: support@talkhao.ai

## License

MIT, for the files in this repository. The Talkhao service is covered by its [terms](https://talkhao.ai/terms).
