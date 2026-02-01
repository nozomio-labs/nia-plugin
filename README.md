# Nia Plugin for Claude Code

Index and search code repositories, documentation, research papers, and HuggingFace datasets with [Nia AI](https://trynia.ai).

## What is Nia?

Nia provides tools for indexing and searching external repositories, research papers, documentation, packages, and performing AI-powered research. Its primary goal is to reduce hallucinations in LLMs and provide up-to-date context for AI agents.

## Installation

### From Marketplace

```bash
/install nia
```

### From GitHub

```bash
/plugin marketplace add nozomio-labs/nia-plugin
/plugin install nia@nozomio-labs/nia-plugin
```

## Setup

1. Get your API key:
   - Run `npx nia-wizard@latest` (guided setup)
   - Or sign up at [trynia.ai](https://trynia.ai)

2. Store the key:
   ```bash
   mkdir -p ~/.config/nia
   echo "your-api-key" > ~/.config/nia/api_key
   ```

3. Requirements: `curl`, `jq`

## What's Included

### Scripts

| Script | Description |
|--------|-------------|
| `repos-list.sh` | List indexed repositories |
| `repos-index.sh` | Index a GitHub repository |
| `repos-tree.sh` | Get repository file tree |
| `repos-read.sh` | Read file from repository |
| `repos-grep.sh` | Search code in repository |
| `sources-list.sh` | List indexed data sources |
| `sources-index.sh` | Index documentation URL |
| `sources-tree.sh` | Get source tree |
| `sources-read.sh` | Read from source |
| `papers-list.sh` | List indexed papers |
| `papers-index.sh` | Index arXiv paper |
| `datasets-list.sh` | List HuggingFace datasets |
| `datasets-index.sh` | Index HuggingFace dataset |
| `search-universal.sh` | Search all indexed sources |
| `search-web.sh` | Web search |
| `search-deep.sh` | Deep research (Pro) |
| `package-grep.sh` | Search package source code |
| `global-subscribe.sh` | Subscribe to public source |
| `oracle.sh` | Run autonomous research (Pro) |

## Usage

```bash
# List indexed repositories
./scripts/repos-list.sh

# Index a repository
./scripts/repos-index.sh "owner/repo"

# Search all indexed sources
./scripts/search-universal.sh "how does auth work?"

# Index documentation
./scripts/sources-index.sh "https://docs.stripe.com"

# Grep repository code
./scripts/repos-grep.sh "vercel/ai" "streamText"
```

## Documentation

See [skills/nia/SKILL.md](./skills/nia/SKILL.md) for the complete workflow guide.

## License

MIT
