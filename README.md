# Flipper Zero Projects

My collection of Flipper Zero apps, signals, and tools.

## Structure

```
flipper/
├── apps/           # Custom FAP applications (C)
├── subghz/         # Sub-GHz signals (.sub)
│   ├── gates/
│   ├── garage-doors/
│   ├── remotes/
│   └── misc/
├── infrared/       # IR remote files (.ir)
│   ├── tvs/
│   ├── ac-units/
│   ├── projectors/
│   ├── led-strips/
│   └── misc/
├── nfc/            # NFC dumps and files
├── rfid/           # 125 kHz RFID files
├── badusb/         # Bad USB payloads
│   ├── claude-installer/  # Auto-install Claude Code + plugins
│   ├── windows/
│   ├── macos/
│   └── linux/
├── animations/     # Custom Flipper animations
└── tools/          # Helper scripts
```

## Featured Payloads

### Claude Code Auto-Installer
Automatically installs [Claude Code](https://claude.ai/code) CLI with plugins on any machine:

| Payload | Target | What it installs |
|---------|--------|------------------|
| `badusb/claude-installer/claude-macos.txt` | macOS | Claude Code + Ralph Loop + Claudeception |
| `badusb/claude-installer/claude-windows.txt` | Windows | Claude Code + Ralph Loop + Claudeception |
| `badusb/claude-installer/claude-linux.txt` | Linux | Claude Code + Ralph Loop + Claudeception |

## Installation

Copy the contents of each folder to the corresponding location on your Flipper Zero SD card:

| Folder | SD Card Path |
|--------|--------------|
| `subghz/` | `/ext/subghz/` |
| `infrared/` | `/ext/infrared/` |
| `nfc/` | `/ext/nfc/` |
| `rfid/` | `/ext/lfrfid/` |
| `badusb/` | `/ext/badusb/` |
| `apps/*.fap` | `/ext/apps/` |

## Resources

- [Official Flipper Docs](https://docs.flipper.net/)
- [Flipper Developer Docs](https://developer.flipper.net/)
- [awesome-flipperzero](https://github.com/djsime1/awesome-flipperzero)
- [Flipper-IRDB](https://github.com/Lucaslhm/Flipper-IRDB)

## License

MIT
