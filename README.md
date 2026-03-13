# karabiner-config

![Delivery of the Keys](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b4/Entrega_de_las_llaves_a_San_Pedro_%28Perugino%29.jpg/700px-Entrega_de_las_llaves_a_San_Pedro_%28Perugino%29.jpg)

*"Delivery of the Keys" (1481-1482) by Pietro Perugino -- [Wikipedia](https://en.wikipedia.org/wiki/Delivery_of_the_Keys_(Perugino))*

**Turning macOS into a well-behaved Emacs citizen.**

A custom [Karabiner Elements](https://karabiner-elements.pqrs.org/) configuration that brings Emacs-style keybindings system-wide on macOS and provides single-keystroke application launchers. If your fingers already think in `C-f`, `C-n`, and `C-x C-s`, this config makes the rest of your OS speak the same language.

## Profiles

Three profiles optimized for different keyboards:

| Profile | Keyboard |
|---|---|
| `mac-default` | Built-in MacBook keyboard |
| `logi-ergonomic` | Logitech Ergo K860 |
| `glove80` | MoErgo Glove80 split keyboard |

## Features

### Application Launchers

Launch apps instantly with `Right Option` + key:

| Shortcut | Application |
|---|---|
| `Right Option + f` | Emacs |
| `Right Option + a` | iTerm2 |
| `Right Option + d` | Brave Browser |
| `Right Option + s` | Google Chrome (automated test instance) |
| `Right Option + w` | Balance (localhost:3005) |
| `Right Option + v` | Slack |
| `Right Option + c` | Signal |
| `Right Option + x` | Messages |
| `Right Option + t` | VLC Player |
| `Right Option + g` | Preview |

### Emacs Keybindings

Comprehensive Emacs keybindings that work across all macOS applications. Emacs and Terminal are excluded so their native bindings are preserved.

#### Navigation

| Shortcut | Action |
|---|---|
| `C-f` | Forward character |
| `C-b` | Backward character |
| `C-n` | Next line |
| `C-p` | Previous line |
| `C-a` | Beginning of line |
| `C-e` | End of line |
| `M-f` | Forward word |
| `M-b` | Backward word |
| `C-v` | Page down |
| `M-v` | Page up |
| `M-<` | Beginning of document |
| `M->` | End of document |

#### Editing

| Shortcut | Action |
|---|---|
| `C-d` | Delete forward |
| `C-h` | Delete backward |
| `C-k` | Kill line |
| `M-d` | Delete word forward |
| `C-w` | Cut |
| `M-w` | Copy |
| `C-y` | Paste |
| `C-/` | Undo |

#### C-x Prefix Commands

| Shortcut | Action |
|---|---|
| `C-x C-s` | Save |
| `C-x C-f` | Open file |
| `C-x C-c` | Quit application |
| `C-x k` | Close tab |
| `C-x h` | Select all |
| `C-x u` | Undo |

#### Clipboard Integration

`M-y` is remapped to `Ctrl+Option+Cmd+Y` outside Emacs to trigger [Maccy](https://maccy.app/) (clipboard manager). Inside Emacs, `M-y` passes through untouched and triggers `counsel-yank-pop` as usual. Both share the system clipboard, so the kill ring and Maccy stay in sync.

#### Control Key Emulations

| Shortcut | Action |
|---|---|
| `C-i` | Tab |
| `C-m` | Return / Enter |
| `C-[` | Escape |
| `C-]` | Escape |

#### Other Shortcuts

| Shortcut | Action |
|---|---|
| `C-g` | Escape / Cancel |
| `C-s` | Search (in supported apps) |
| `C-t` | New tab |
| `C-l` | Focus URL bar (browsers) |
| `C-z` | Undo |

## Design Principles

- **Home row focused** -- minimize finger travel
- **Touch typing friendly** -- leverage muscle memory
- **Emacs everywhere** -- consistent keybindings across macOS
- **Keyboard agnostic** -- works with built-in, external, and split keyboards

## Installation

1. Install [Karabiner Elements](https://karabiner-elements.pqrs.org/)
2. Clone this repository
3. Symlink or copy `karabiner.json` to `~/.config/karabiner/karabiner.json`:

```bash
ln -sf $(pwd)/karabiner.json ~/.config/karabiner/karabiner.json
```

## Related

- [emacs-config](https://github.com/pdelfino/emacs-config) -- The Emacs setup these keybindings complement
- [homerow-config](https://github.com/pdelfino/homerow-config) -- Click things without a mouse
- [my-shortkeys-config](https://github.com/pdelfino/my-shortkeys-config) -- Emacs-style shortcuts in the browser
- [claude-config](https://github.com/pdelfino/claude-config) -- Claude Code configuration
- [iterm2-config](https://github.com/pdelfino/iterm2-config) -- iTerm2 terminal profile
- [zshrc](https://github.com/pdelfino/zshrc) -- Shell configuration with Emacs keybindings
- [macos-setup](https://github.com/pdelfino/macos-setup) -- The bootstrap that ties it all together

## License

MIT
