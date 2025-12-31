# Zellij Configuration Layout Visualizations

## 28-Inch Monitor Configuration

### Tab 1: AI & Terminal (Default/Focus)
```
┌─────────────────────────────────────────────────────────────────┐
│ Tab Bar: [AI & Terminal] [System Information] [Development]    │
├─────────────────────────────────────────────────────────────────┤
│                                           │                     │
│                                           │                     │
│                                           │                     │
│          AI Assistant (70%)               │   Terminal (30%)    │
│                                           │                     │
│                                           │                     │
│                                           │                     │
├─────────────────────────────────────────────────────────────────┤
│ Status Bar                                                      │
└─────────────────────────────────────────────────────────────────┘
```

### Tab 2: System Information
```
┌─────────────────────────────────────────────────────────────────┐
│ Tab Bar: [AI & Terminal] [System Information] [Development]    │
├──────────────────────────────┬──────────────────────────────────┤
│                              │                                  │
│                              │                                  │
│   System Monitor (htop)      │   Process Monitor (watch ps)     │
│                              │                                  │
│                              │                                  │
├──────────────────────────────┼──────────────────────────────────┤
│                              │                                  │
│                              │                                  │
│   System Logs (tail -f)      │   Notes (vim/nano)               │
│                              │                                  │
│                              │                                  │
├─────────────────────────────────────────────────────────────────┤
│ Status Bar                                                      │
└─────────────────────────────────────────────────────────────────┘
```

### Tab 3: Development
```
┌─────────────────────────────────────────────────────────────────┐
│ Tab Bar: [AI & Terminal] [System Information] [Development]    │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│                                                                 │
│                   Code Editor                                   │
│                                                                 │
│                                                                 │
├──────────────────────────────┬──────────────────────────────────┤
│                              │                                  │
│   File Explorer              │   Git Status                     │
│   (ranger/mc/ls)             │   (watch git status)             │
│                              │                                  │
├─────────────────────────────────────────────────────────────────┤
│ Status Bar                                                      │
└─────────────────────────────────────────────────────────────────┘
```

---

## 15-Inch MacBook Configuration

### Tab 1: AI & Terminal (Default/Focus)
```
┌────────────────────────────────────────────────────┐
│ Tab Bar: [AI & Terminal] [System] [Development]   │
├────────────────────────────────────────────────────┤
│                              │                     │
│                              │                     │
│    AI Assistant (65%)        │  Terminal (35%)     │
│                              │                     │
│                              │                     │
├────────────────────────────────────────────────────┤
│ Status Bar                                         │
└────────────────────────────────────────────────────┘
```

### Tab 2: System Information (Simplified)
```
┌────────────────────────────────────────────────────┐
│ Tab Bar: [AI & Terminal] [System] [Development]   │
├───────────────────────┬────────────────────────────┤
│                       │                            │
│                       │                            │
│  System Monitor       │   Notes & Tasks            │
│  (htop/top)           │   (vim/nano)               │
│                       │                            │
│                       │                            │
│                       │                            │
├────────────────────────────────────────────────────┤
│ Status Bar                                         │
└────────────────────────────────────────────────────┘
```

### Tab 3: Development (Simplified)
```
┌────────────────────────────────────────────────────┐
│ Tab Bar: [AI & Terminal] [System] [Development]   │
├────────────────────────────────────────────────────┤
│                                                    │
│                                                    │
│           Code Editor (70%)                        │
│                                                    │
│                                                    │
├────────────────────────────────────────────────────┤
│                                                    │
│       Terminal & Git (30%)                         │
│                                                    │
├────────────────────────────────────────────────────┤
│ Status Bar                                         │
└────────────────────────────────────────────────────┘
```

---

## Side-by-Side Comparison

### Complexity Comparison

**28-Inch Monitor:**
- Tab 1: **2 panes** (70/30 horizontal split)
- Tab 2: **4 panes** (2x2 grid)
- Tab 3: **3 panes** (1 large top, 2 bottom)
- **Total: 9 panes across 3 tabs**

**15-Inch MacBook:**
- Tab 1: **2 panes** (65/35 horizontal split)
- Tab 2: **2 panes** (50/50 horizontal split)
- Tab 3: **2 panes** (70/30 vertical split)
- **Total: 6 panes across 3 tabs**

### Key Differences

| Feature | 28-Inch | 15-Inch |
|---------|---------|---------|
| **System Info Panes** | 4 (htop, processes, logs, notes) | 2 (htop, notes) |
| **Development Panes** | 3 (editor, explorer, git) | 2 (editor, terminal) |
| **AI Assistant Split** | 70/30 | 65/35 |
| **Readability** | More info visible | Less cluttered |
| **Resource Usage** | Higher (more panes) | Lower (fewer panes) |
| **Best Use Case** | Desktop workstation | Portable laptop work |

### Workflow Recommendations

**Use 28-Inch config when:**
- Working on a desktop with large monitor
- Need to monitor multiple systems simultaneously
- Want to see logs, processes, and code at once
- Have plenty of screen real estate

**Use 15-Inch config when:**
- Working on MacBook or laptop
- Need focused, less cluttered workspace
- Want better readability on smaller screen
- Battery/performance is a concern

### Quick Reference

**Tab Navigation (Both configs):**
- `Alt + 1` → AI & Terminal
- `Alt + 2` → System Information
- `Alt + 3` → Development

**Mode Switching:**
- `Ctrl + p` → Pane mode (resize, move, close panes)
- `Ctrl + t` → Tab mode (create, rename, close tabs)
- `Ctrl + n` → Normal mode (back to normal)
