# Claude Code Configuration

This repository contains my personal Claude Code configuration and customizations.

## Contents

- **settings.json** - Main Claude Code settings including permissions and hooks
- **settings.local.json** - Local settings overrides
- **agents/** - Custom AI agents for specialized tasks
- **commands/** - Custom CLI commands
- **hooks/** - Event hooks for session management and automation
- **output-styles/** - Custom output formatting styles
- **status_lines/** - Custom status line configurations
- **todos/** - Todo management configurations
- **plugins/** - Plugin configurations

## Features

### Custom Agents
The `agents/` folder contains specialized AI agents for various tasks including:
- Cryptocurrency market analysis
- Todo management
- Code review and optimization
- And more...

### Hooks & Automation
- Session start hooks for initialization
- Custom status line showing current context
- Automated task tracking

### Permissions
Configured with specific tool permissions for secure operation.

## Setup

1. Clone this repository to your `~/.claude` directory
2. Copy `.env.example` to `.env` and add your API keys
3. Restart Claude Code to load the configuration

## Note

Sensitive files like `.env`, logs, and project caches are excluded from version control for security.