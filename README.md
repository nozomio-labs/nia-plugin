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

| Category | Scripts |
|----------|---------|
| **Repositories** | `repos-list.sh`, `repos-index.sh`, `repos-tree.sh`, `repos-read.sh`, `repos-grep.sh`, `repos-status.sh` |
| **Data Sources** | `sources-list.sh`, `sources-index.sh`, `sources-tree.sh`, `sources-ls.sh`, `sources-read.sh`, `sources-grep.sh` |
| **Research Papers** | `papers-list.sh`, `papers-index.sh` |
| **HuggingFace Datasets** | `datasets-list.sh`, `datasets-index.sh` |
| **Search** | `search-query.sh`, `search-universal.sh`, `search-web.sh`, `search-deep.sh` |
| **Package Search** | `package-grep.sh`, `package-hybrid.sh`, `package-read.sh` |
| **Global Sources** | `global-subscribe.sh` |
| **Oracle Research** | `oracle.sh`, `oracle-job.sh`, `oracle-job-status.sh`, `oracle-jobs-list.sh`, `oracle-sessions.sh` |
| **Usage** | `usage.sh` |

## Usage Examples

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

# Query specific repos/docs
./scripts/search-query.sh "explain hooks" "facebook/react,vercel/next.js" "React Docs"

# Index an arXiv paper
./scripts/papers-index.sh "2312.00752"

# Index a HuggingFace dataset
./scripts/datasets-index.sh "squad"

# Run Oracle research job
./scripts/oracle-job.sh "compare React vs Vue state management"

# Check API usage
./scripts/usage.sh
```

## Source Types

| Type | Index Method | Identifier Formats |
|------|--------------|-------------------|
| Repository | `repos-index.sh` | `owner/repo` |
| Documentation | `sources-index.sh` | `https://docs.example.com` |
| Research Paper | `papers-index.sh` | `2312.00752`, arXiv URL |
| HuggingFace Dataset | `datasets-index.sh` | `squad`, `owner/dataset` |

## Flexible Identifiers

Most data source endpoints accept:
- **UUID**: `550e8400-e29b-41d4-a716-446655440000`
- **Display name**: `Vercel AI SDK - Core`, `openai/gsm8k`
- **URL**: `https://docs.trynia.ai/`, `https://arxiv.org/abs/2312.00752`

## Documentation

See [skills/nia/SKILL.md](./skills/nia/SKILL.md) for the complete workflow guide.

## License

MIT
