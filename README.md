# Claude Code Configuration

This repository contains my personal Claude Code configuration and customizations.

## Table of Contents

- [Overview](#overview)
- [Custom Agents](#custom-agents)
- [Output Styles](#output-styles)
- [Configuration Files](#configuration-files)
- [Hooks & Automation](#hooks--automation)
- [Setup](#setup)

## Overview

A comprehensive Claude Code setup featuring specialized AI agents, custom output formatting, automation hooks, and intelligent task management.

## Custom Agents

Specialized AI agents for various tasks and domains:

### Crypto Analysis Agents

**Market Overview & Analysis:**
- [`crypto-market-agent-haiku`](agents/crypto/crypto-market-agent-haiku.md) - Real-time market data for top cryptocurrencies (Haiku model)
- [`crypto-market-agent-sonnet`](agents/crypto/crypto-market-agent-sonnet.md) - Market analysis with balanced speed/detail (Sonnet model)  
- [`crypto-market-agent-opus`](agents/crypto/crypto-market-agent-opus.md) - In-depth market analysis (Opus model)

**Individual Coin Analysis:**
- [`crypto-coin-analyzer-haiku`](agents/crypto/crypto-coin-analyzer-haiku.md) - Fast coin-specific analysis and sentiment
- [`crypto-coin-analyzer-sonnet`](agents/crypto/crypto-coin-analyzer-sonnet.md) - Detailed coin analysis with technical indicators
- [`crypto-coin-analyzer-opus`](agents/crypto/crypto-coin-analyzer-opus.md) - Comprehensive coin research and analysis

**Investment & Trading:**
- [`crypto-investment-plays-haiku`](agents/crypto/crypto-investment-plays-haiku.md) - Quick investment opportunities identification
- [`crypto-investment-plays-sonnet`](agents/crypto/crypto-investment-plays-sonnet.md) - Actionable investment strategies with risk analysis
- [`crypto-investment-plays-opus`](agents/crypto/crypto-investment-plays-opus.md) - Comprehensive investment research and plays

**Market Movement & Correlations:**
- [`crypto-movers-haiku`](agents/crypto/crypto-movers-haiku.md) - Track biggest gainers and losers across timeframes
- [`macro-crypto-correlation-scanner-haiku`](agents/crypto/macro-crypto-correlation-scanner-haiku.md) - Quick macro/crypto correlation analysis
- [`macro-crypto-correlation-scanner-sonnet`](agents/crypto/macro-crypto-correlation-scanner-sonnet.md) - Fed policy and traditional market impacts on crypto
- [`macro-crypto-correlation-scanner-opus`](agents/crypto/macro-crypto-correlation-scanner-opus.md) - Deep macro-economic crypto correlation analysis

### General Utility Agents

**Task Management & Workflow:**
- [`todo-agent`](agents/todo-agent.md) - Intelligent todo detection and persistent task management
- [`work-completion-summary`](agents/work-completion-summary.md) - Audio summaries and next steps suggestions

**Development & Research:**
- [`meta-agent`](agents/meta-agent.md) - Generates new Claude Code agent configurations from descriptions
- [`llm-ai-agents-and-eng-research`](agents/llm-ai-agents-and-eng-research.md) - Latest AI/ML news and engineering developments

**Interaction & Communication:**
- [`hello-world-agent`](agents/hello-world-agent.md) - Friendly greetings with tech news updates

## Output Styles

Custom formatting styles for different types of responses and use cases:

### Structured Formats
- [`bullet-points`](output-styles/bullet-points.md) - Hierarchical bullet points for quick scanning and digestible information
- [`table-based`](output-styles/table-based.md) - Tabular format for comparative data and structured information
- [`yaml-structured`](output-styles/yaml-structured.md) - YAML formatting for configuration-like outputs
- [`html-structured`](output-styles/html-structured.md) - HTML markup for rich formatting and web-ready content

### Communication Styles  
- [`markdown-focused`](output-styles/markdown-focused.md) - Clean markdown formatting optimized for documentation
- [`ultra-concise`](output-styles/ultra-concise.md) - Minimal, direct responses for quick answers
- [`tts-summary`](output-styles/tts-summary.md) - Audio task completion announcements with text-to-speech

### Specialized Applications
- [`genui`](output-styles/genui.md) - UI/UX focused formatting for design and interface work

## Configuration Files

Core configuration and settings:

- **[settings.json](settings.json)** - Main Claude Code settings including permissions and hooks
- **[settings.local.json](settings.local.json)** - Local settings overrides
- **[.gitignore](.gitignore)** - Excludes sensitive files and temporary data

### Directory Structure
- **agents/** - Custom AI agents for specialized tasks
- **commands/** - Custom CLI commands and agent prompts
- **hooks/** - Event hooks for session management and automation  
- **output-styles/** - Custom output formatting styles
- **status_lines/** - Custom status line configurations
- **plugins/** - Plugin configurations

## Hooks & Automation

Automated workflows and session management:

- **Session start hooks** - Initialize environment and load configurations
- **Custom status line** - Shows current context and system status
- **Automated task tracking** - Intelligent todo detection and management
- **TTS notifications** - Audio feedback for task completion
- **Pre/post tool use hooks** - Workflow automation around tool usage

## Setup

1. Clone this repository to your `~/.claude` directory
2. Copy `.env.example` to `.env` and add your API keys
3. Restart Claude Code to load the configuration

## Note

Sensitive files like `.env`, logs, and project caches are excluded from version control for security.