# Kasane Teto VS Code Theme (重音テト) 🥖

A vibrant dark VS Code theme inspired by **Kasane Teto** (UTAU / Synthesizer V).

<p align="center">
  <img src="assets/icon.png" alt="Kasane Teto Icon" width="128" />
</p>

## 📸 Preview

![Kasane Teto Theme Preview](assets/preview.png)

## 🎨 Color Palette

| Color | Hex | RGB | Usage |
| :--- | :--- | :--- | :--- |
| **Point Accent** | `#ff0045` | `(255, 0, 69)` | Primary point color: cursor, active tab border, focus rings, buttons, function names |
| **Secondary Pink** | `#eda7ba` | `(237, 167, 186)` | Strings, parameters, JSON keys, tag attributes, active line numbers |
| **Slate Grey (Canvas)** | `#252a32` | `(37, 42, 50)` | Main editor canvas & panels |
| **Slate Grey (Borders)** | `#3f4750` | `(63, 71, 80)` | Structural borders, dividers, guide lines, inactive elements |
| **Vibrant Magenta** | `#d924d5` | `(217, 36, 213)` | Keywords, control flow, operators, storage types |
| **Midnight Navy** | `#06053b` | `(6, 5, 59)` | Deep contrasting tone |

---

## 🚀 Installation

### Option 1: VS Code Marketplace
Install directly from the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=SinsuSquid.kasane-teto-theme) or via command line:

```bash
code --install-extension SinsuSquid.kasane-teto-theme
```

### Option 2: Local Development Link (Instant Hot-Reload)
Link the repository directly into your VS Code extensions folder:

```bash
ln -sfn "$(pwd)" ~/.vscode/extensions/kasane-teto-theme
```

Then in VS Code:
1. Press `Ctrl+Shift+P` (or `Cmd+Shift+P` on macOS) and run `Developer: Reload Window`.
2. Press `Ctrl+K Ctrl+T` and select **Kasane Teto Dark**.

### Option 3: Install from .vsix Package
```bash
code --install-extension kasane-teto-theme-0.1.0.vsix
```

---

## 🥖 Features
- **High Readability**: High-contrast syntax highlighting fine-tuned for TypeScript, JavaScript, Python, Rust, Go, HTML/CSS, JSON, and Markdown.
- **Kasane Teto Aesthetics**: Features the sitting plushie icon with a transparent background.

---

## 🚀 Starship Prompt Theme

A companion Starship prompt configured with Kasane Teto colors and baguette (`🥖`) character!

### Quick Setup
```bash
# Step 1: copy the theme config
mkdir -p ~/.config/starship
ln -sfn "$(pwd)/starship/starship.toml" ~/.config/starship/kasane-teto.toml

# Step 2: source the shell environment (sets STARSHIP_CONFIG, FZF & LS_COLORS)
# Add this to your ~/.bashrc or ~/.zshrc:
source "$(pwd)/starship/teto.env.sh"
```

---

## ⚡ Vim / Neovim Theme

A companion colorscheme and **vim-airline** theme for Vim and Neovim.

### Quick Setup
```bash
# Link colorscheme
mkdir -p ~/.vim/colors ~/.vim/autoload/airline/themes
ln -sfn "$(pwd)/vim/colors/kasane-teto.vim" ~/.vim/colors/kasane-teto.vim
ln -sfn "$(pwd)/vim/autoload/airline/themes/kasane_teto.vim" ~/.vim/autoload/airline/themes/kasane_teto.vim
```

In your `.vimrc` or `init.vim`:
```vim
colorscheme kasane-teto
let g:airline_theme = 'kasane_teto'
```

---

## 🪟 tmux Theme

A companion status bar and interface theme for **tmux**.

### Quick Setup
```bash
# Link tmux configuration
ln -sfn "$(pwd)/tmux/kasane-teto.tmux.conf" ~/.config/kasane-teto.tmux.conf
```

Add to your `~/.tmux.conf`:
```tmux
source-file ~/.config/kasane-teto.tmux.conf
```

---

## 📊 btop Theme

A companion system monitor theme for **btop**.

### Quick Setup
```bash
# Link btop theme
mkdir -p ~/.config/btop/themes
ln -sfn "$(pwd)/btop/kasane-teto.theme" ~/.config/btop/themes/kasane-teto.theme
```

In `~/.config/btop/btop.conf`:
```ini
color_theme = "$HOME/.config/btop/themes/kasane-teto.theme"
```

---

## 💻 Windows Terminal Theme

A companion color scheme for **Windows Terminal**.

### Quick Setup

#### Option 1: Add to `settings.json`
Add the scheme from [`windows-terminal/kasane-teto.json`](windows-terminal/kasane-teto.json) to the `schemes` array in your Windows Terminal `settings.json` (`Ctrl+Shift+,`):

```json
{
  "name": "Kasane Teto",
  "cursorColor": "#ff0045",
  "selectionBackground": "#ff0045",
  "background": "#1e2228",
  "foreground": "#f0eef5",
  "black": "#252a32",
  "red": "#ff0045",
  "green": "#3ddc97",
  "yellow": "#f9c74f",
  "blue": "#5c7cfa",
  "purple": "#d924d5",
  "cyan": "#00f0ff",
  "white": "#f0eef5",
  "brightBlack": "#4d5663",
  "brightRed": "#ff336a",
  "brightGreen": "#52f2ab",
  "brightYellow": "#ffe066",
  "brightBlue": "#748ffc",
  "brightPurple": "#e84df2",
  "brightCyan": "#5efcff",
  "brightWhite": "#ffffff"
}
```

Then select **Kasane Teto** in your profile settings or set in `profiles.defaults`:
```json
"colorScheme": "Kasane Teto"
```

#### Option 2: JSON Fragment Extension
Copy [`windows-terminal/kasane-teto-fragment.json`](windows-terminal/kasane-teto-fragment.json) to your Windows Terminal Fragments directory:
```powershell
New-Item -ItemType Directory -Force "$env:LOCALAPPDATA\Microsoft\Windows Terminal\Fragments\KasaneTeto"
Copy-Item "windows-terminal\kasane-teto-fragment.json" "$env:LOCALAPPDATA\Microsoft\Windows Terminal\Fragments\KasaneTeto\kasane-teto.json"
```

---

## 🐱 Kitty Terminal Theme

A companion colorscheme for **Kitty**.

### Quick Setup

```bash
# Link kitty theme
mkdir -p ~/.config/kitty/themes
ln -sfn "$(pwd)/kitty/kasane-teto.conf" ~/.config/kitty/themes/kasane-teto.conf
```

Add to your `~/.config/kitty/kitty.conf`:
```conf
include themes/kasane-teto.conf
```

Or apply directly via the Kitty theme kitten:
```bash
kitty +kitten themes --reload-in=all Kasane\ Teto
```
