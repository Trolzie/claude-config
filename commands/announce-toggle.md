# Announce Toggle

Toggle announcement settings for Claude Code session startup.

## Usage

```
/announce-toggle
```

## Description

This command toggles the TTS (Text-to-Speech) announcement feature that speaks when Claude Code sessions start. The setting persists across sessions.

When announcements are enabled, you'll hear:
- "Claude Code session started" on startup
- "Resuming previous session" on resume
- "Starting fresh session" on clear

## Implementation

```python
#!/usr/bin/env -S uv run --script
# /// script
# requires-python = ">=3.11"
# dependencies = []
# ///

import json
import sys
from pathlib import Path

def main():
    # Path to settings file
    settings_dir = Path.home() / ".claude" / "data"
    settings_dir.mkdir(parents=True, exist_ok=True)
    settings_file = settings_dir / "announce-settings.json"
    
    # Read current setting
    if settings_file.exists():
        try:
            with open(settings_file, 'r') as f:
                settings = json.load(f)
            current_enabled = settings.get('announcements_enabled', False)
        except (json.JSONDecodeError, KeyError):
            current_enabled = False
    else:
        current_enabled = False
    
    # Toggle the setting
    new_enabled = not current_enabled
    
    # Save the new setting
    settings = {'announcements_enabled': new_enabled}
    with open(settings_file, 'w') as f:
        json.dump(settings, f, indent=2)
    
    # Display status
    if new_enabled:
        print("✅ Announcements enabled")
        print("Claude Code will now announce session starts via TTS")
    else:
        print("❌ Announcements disabled")
        print("Claude Code will start silently")
    
if __name__ == '__main__':
    main()
```