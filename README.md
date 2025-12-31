# Zellij Configuration Files

This repository contains optimized Zellij configurations for different display sizes.

## Directory Structure

```
zellij-config/
├── configs/
│   ├── 28-inch/          # Configuration for 28" monitor
│   │   ├── config.kdl
│   │   └── layouts/
│   │       └── all_workspaces.kdl
│   └── 15-inch/          # Configuration for 15" MacBook
│       ├── config.kdl
│       └── layouts/
│           └── all_workspaces.kdl
└── README.md
```

## Configuration Differences

### 28-Inch Monitor Configuration
**Optimized for:** Large desktop monitors with plenty of screen real estate

**Features:**
- **AI & Terminal Tab:** 70/30 split for maximum AI assistant workspace
- **System Information Tab:** 4-pane grid layout with:
  - System Monitor (htop)
  - Process Monitor (real-time CPU usage)
  - System Logs (live log viewer)
  - Notes (vim/nano editor)
- **Development Tab:** 3-pane layout with code editor, file explorer, and git status

**Best for:** Desktop workstation with large monitor where you want to see multiple panes simultaneously

### 15-Inch MacBook Configuration
**Optimized for:** Laptop displays where screen space is limited

**Features:**
- **AI & Terminal Tab:** 65/35 split for balanced view
- **System Information Tab:** Simplified 2-pane layout with:
  - System Monitor (htop/top)
  - Notes & Tasks
- **Development Tab:** Clean 2-pane vertical split (70/30) for focused coding

**Best for:** MacBook or smaller laptop screens where fewer panes improve readability

## Installation Instructions

### For 28-Inch Monitor (WSL/Linux)

```bash
# Backup existing config (if any)
mv ~/.config/zellij ~/.config/zellij.backup

# Copy 28-inch config
mkdir -p ~/.config/zellij
cp -r ~/Coding/zellij-config/configs/28-inch/* ~/.config/zellij/

# Verify installation
ls -la ~/.config/zellij
```

### For 15-Inch MacBook

```bash
# Clone the repository (if not already done)
git clone https://github.com/cjjamesd/zellij-config.git
cd zellij-config

# Backup existing config (if any)
mv ~/.config/zellij ~/.config/zellij.backup

# Copy 15-inch config
mkdir -p ~/.config/zellij
cp -r configs/15-inch/* ~/.config/zellij/

# Verify installation
ls -la ~/.config/zellij
```

### Start Zellij

```bash
# Start zellij with your new configuration
zellij

# Or create a named session
zellij -s mysession
```

## Switching Between Configurations

If you use both a laptop and external monitor, you can easily switch:

```bash
# For 28-inch monitor
cp -r ~/Coding/zellij-config/configs/28-inch/* ~/.config/zellij/

# For 15-inch laptop
cp -r ~/Coding/zellij-config/configs/15-inch/* ~/.config/zellij/

# Restart zellij to apply changes
zellij kill-all-sessions
zellij
```

## Quick Installation Script

Create this script to quickly switch configs:

**switch-zellij-config.sh:**
```bash
#!/bin/bash

echo "Select Zellij Configuration:"
echo "1) 28-inch Monitor"
echo "2) 15-inch MacBook"
read -p "Enter choice (1 or 2): " choice

case $choice in
    1)
        cp -r ~/Coding/zellij-config/configs/28-inch/* ~/.config/zellij/
        echo "Switched to 28-inch configuration"
        ;;
    2)
        cp -r ~/Coding/zellij-config/configs/15-inch/* ~/.config/zellij/
        echo "Switched to 15-inch configuration"
        ;;
    *)
        echo "Invalid choice"
        exit 1
        ;;
esac

echo "Restart zellij to apply changes: zellij kill-all-sessions && zellij"
```

Make it executable:
```bash
chmod +x switch-zellij-config.sh
```

## Key Bindings (Same for Both Configs)

### Mode Switching
- `Ctrl + a` - Session mode
- `Ctrl + g` - Resize mode
- `Ctrl + p` - Pane mode
- `Ctrl + t` - Tab mode
- `Ctrl + n` - Normal mode

### Quick Tab Navigation
- `Alt + 1` - Go to tab 1 (AI & Terminal)
- `Alt + 2` - Go to tab 2 (System Information)
- `Alt + 3` - Go to tab 3 (Development)

### Session Management
- `Ctrl + d` - Detach from session (in session mode)
- `Ctrl + q` - Quit zellij (in session mode)

## Tips for Comparison Testing

When testing on your MacBook tonight:

1. **Try both configs** on your MacBook to see which you prefer
2. **Check readability** - can you comfortably read all panes?
3. **Test with real workflows** - open your actual development tools
4. **Resize panes** - use `Ctrl + g` to adjust if needed
5. **Note performance** - more panes = more resource usage

## Customization

Feel free to modify these configs! The main differences to experiment with:

- **Pane sizes:** Adjust the `size="X%"` values
- **Number of panes:** Add or remove pane blocks
- **Commands:** Change what runs in each pane
- **Tab names:** Rename tabs to match your workflow

## Updating from GitHub

```bash
cd ~/Coding/zellij-config
git pull
# Then copy your preferred config as shown above
```

## Contributing

If you create improvements or find better optimizations, commit and push them:

```bash
cd ~/Coding/zellij-config
git add .
git commit -m "Description of changes"
git push
```

## Resources

- [Zellij Documentation](https://zellij.dev/documentation/)
- [Zellij GitHub](https://github.com/zellij-org/zellij)
- [KDL Language Spec](https://kdl.dev/)
