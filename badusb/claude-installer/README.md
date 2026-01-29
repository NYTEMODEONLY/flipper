# Claude Code Auto-Installer

BadUSB payloads that automatically install Claude Code CLI with the Ralph Loop plugin and Claudeception skill.

## What Gets Installed

| Component | Description |
|-----------|-------------|
| **Claude Code** | Anthropic's official CLI for AI-assisted coding |
| **Ralph Loop** | Plugin for continuous self-referential AI loops |
| **Claudeception** | Skill that auto-extracts reusable knowledge from sessions |

## Payloads

| File | Target OS | Terminal Method |
|------|-----------|-----------------|
| `claude-macos.txt` | macOS 13.0+ | Spotlight → Terminal |
| `claude-windows.txt` | Windows 10/11 | Win+R → PowerShell |
| `claude-linux.txt` | Ubuntu/Debian | Ctrl+Alt+T |

## Usage

1. Copy the appropriate `.txt` file to your Flipper Zero's SD card:
   ```
   /ext/badusb/claude-installer/
   ```

2. On your Flipper Zero:
   - Go to **Bad USB** app
   - Select the payload for your target OS
   - Connect to target machine via USB
   - Press **Run**

3. The payload will:
   - Open a terminal/PowerShell
   - Install Claude Code CLI
   - Install Ralph Loop plugin
   - Clone and configure Claudeception
   - Set up the activation hook

## Timing Notes

Default delays are tuned for typical machines. Adjust `DELAY` values if:
- **Slower machine**: Increase delays (especially after `curl` commands)
- **Faster machine**: Decrease delays for quicker execution

## Requirements

### macOS
- macOS 13.0 or later
- Internet connection

### Windows
- Windows 10 or 11
- Git for Windows (for Claudeception)
- Internet connection

### Linux
- Ubuntu 20.04+ or Debian 10+
- `curl` and `git` installed
- Internet connection

## Post-Installation

After the payload completes, verify installation:

```bash
claude --version
claude /plugin list
ls ~/.claude/skills/
```

Start using Claude Code:

```bash
claude
```

## Customization

Edit the payloads to:
- Change delays for your target hardware
- Add additional plugins
- Modify the settings configuration
- Add your own skills

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Terminal doesn't open | Adjust opening method (GUI+SPACE, CTRL-ALT-T, etc.) |
| Installation times out | Increase DELAY values |
| Plugin not found | Ensure internet connectivity |
| Claudeception missing | Check if git is installed on target |

## Security Note

These payloads require:
- Physical USB access to target machine
- Active internet connection
- Target machine to be unlocked

## Resources

- [Claude Code Docs](https://code.claude.com/docs)
- [Flipper Zero BadUSB](https://docs.flipper.net/zero/bad-usb)
- [DuckyScript Reference](https://developer.flipper.net/flipperzero/doxygen/badusb_file_format.html)
