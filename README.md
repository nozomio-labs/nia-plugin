# Nia Plugin for Claude Code

A Claude Code plugin that provides the Nia skill for indexing and searching external documentation, repositories, packages, and research papers.

## Installation

### From GitHub (once published)

```bash
/plugin marketplace add nozomio-labs/nia-plugin
/plugin install nia@nozomio-labs/nia-plugin
```

### From Local Path (for development)

```bash
/plugin install /path/to/nia-plugin
```

## Requirements

This plugin requires the Nia MCP server to be configured. Add to your Claude Code settings:

```json
{
  "mcpServers": {
    "nia": {
      "command": "your-nia-server-command",
      "args": []
    }
  }
}
```

## What's Included

### Skills

- **nia** - Guides Claude through the optimal workflow for using Nia tools:
  - Check if sources are indexed
  - Explore source structure with tree/ls
  - Search with semantic and regex tools
  - Save context for reuse across conversations

## Usage

Once installed, invoke the skill:

```
/nia <your query>
```

Or Claude will automatically use it when external documentation or repository searches are needed.

## License

MIT
