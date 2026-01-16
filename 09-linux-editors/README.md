
# Linux Text Editing with Vim

This section covers **text editing using Vim**, a powerful and versatile editor in Linux. All commands are shown in a clean, consistent Markdown format with proper code blocks.

---

## Modes in Vim

| Mode          | Purpose                                                   | How to Enter / Exit          |
|---------------|-----------------------------------------------------------|-----------------------------|
| Normal Mode   | Default mode, used for navigation and command execution  | Press `Esc`                 |
| Insert Mode   | Used for text editing                                     | Press `i` to enter, `Esc` to exit |
| Command Mode  | Used for saving, quitting, and searching                 | Press `:` in Normal mode     |

---

## Basic Navigation

| Command | Action |
|---------|--------|
| `h`     | Move left |
| `l`     | Move right |
| `j`     | Move down |
| `k`     | Move up |
| `0`     | Move to beginning of line |
| `^`     | Move to first non-blank character of line |
| `$`     | Move to end of line |
| `w`     | Move to next word |
| `b`     | Move to previous word |
| `gg`    | Move to start of file |
| `G`     | Move to end of file |
| `:n`    | Move to line number `n` |

---

## Insert Mode Shortcuts

| Command | Action |
|---------|--------|
| `i`     | Insert before cursor |
| `I`     | Insert at beginning of line |
| `a`     | Append after cursor |
| `A`     | Append at end of line |
| `o`     | Open a new line below |
| `O`     | Open a new line above |
| `Esc`   | Exit insert mode |

---

## Editing Text

| Command | Action |
|---------|--------|
| `x`     | Delete a character |
| `X`     | Delete character before cursor |
| `dw`    | Delete a word |
| `dd`    | Delete a line |
| `d$`    | Delete from cursor to end of line |
| `d0`    | Delete from cursor to beginning of line |
| `D`     | Delete from cursor to end of line |
| `u`     | Undo last action |
| `Ctrl + r` | Redo an undone change |
| `yy`    | Copy (yank) a line |
| `yw`    | Copy (yank) a word |
| `p`     | Paste after cursor |
| `P`     | Paste before cursor |

---

## Search and Replace

| Command | Action |
|---------|--------|
| `/pattern` | Search forward for a pattern |
| `?pattern` | Search backward for a pattern |
| `n`       | Repeat last search forward |
| `N`       | Repeat last search backward |
| `:%s/old/new/g` | Replace all occurrences of "old" with "new" |
| `:s/old/new/g`  | Replace all occurrences in the current line |

---

## Working with Multiple Files

| Command | Action |
|---------|--------|
| `:e filename` | Open a new file |
| `:w`          | Save file |
| `:wq`         | Save and exit |
| `:q!`         | Quit without saving |
| `:split filename`  | Split screen horizontally and open another file |
| `:vsplit filename` | Split screen vertically |
| `Ctrl + w + w`    | Switch between split screens |

---

✅ **Vim is a highly efficient editor for Linux systems — mastering its modes, navigation, and editing shortcuts significantly improves productivity.**
