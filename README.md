# Vim tutorial

Vim is a keyboard-driven text editor based on `vi`. This guide covers the commands needed to open a file, move around, make basic edits, and save or quit.

Start Vim with a file:

```bash
vim example.txt
```

Vim behaves differently depending on its current mode. If a command does not work as expected, press `Esc` to return to Normal mode and try again.

## Modes

| Mode | Enter it with | Purpose |
| --- | --- | --- |
| Normal | `Esc` | Move through the file and run editing commands |
| Insert | `i` | Type text before the cursor |
| Visual | `v` | Select text before applying a command |

Vim starts in Normal mode. Most commands in this guide assume that mode unless stated otherwise.

## Save and quit

Press `:` in Normal mode to enter a command on the bottom line, then press `Enter` to run it.

| Command | Result |
| --- | --- |
| `:w` | Save the file |
| `:q` | Quit if there are no unsaved changes |
| `:wq` | Save and quit |
| `:q!` | Quit and discard unsaved changes |

## Move around

### Characters and words

| Key | Movement |
| --- | --- |
| `h` | One character left |
| `j` | One line down |
| `k` | One line up |
| `l` | One character right |
| `b` | Beginning of the current or previous word |
| `e` | End of the current or next word |
| `w` | Beginning of the next word |
| `0` | Beginning of the line |
| `$` | End of the line |

Add a count before a movement to repeat it. For example, `4l` moves four characters right and `2b` moves backward by two words.

### Files, lines, and matching characters

| Command | Movement |
| --- | --- |
| `gg` | First line of the file |
| `G` | Last line of the file |
| `36G` | Line 36 |
| `%` | Matching `()`, `[]`, or `{}` character |
| `*` | Next occurrence of the word under the cursor |
| `#` | Previous occurrence of the word under the cursor |

## Search

Type `/text` in Normal mode and press `Enter` to search forward for `text`.

| Key | Result |
| --- | --- |
| `n` | Next match in the same search direction |
| `N` | Previous match |

## Insert text

| Command | Where Insert mode starts |
| --- | --- |
| `i` | Before the cursor |
| `I` | At the first non-blank character of the line |
| `a` | After the cursor |
| `A` | At the end of the line |
| `o` | On a new line below the current line |
| `O` | On a new line above the current line |

Press `Esc` when you are done typing. A count also works with insertion: type `6i-`, then press `Esc`, to insert `------`.

## Delete or change text

Vim combines an operator such as `d` with a movement such as `w`. Counts can come before the operator or movement.

| Command | Result |
| --- | --- |
| `x` | Delete the character under the cursor |
| `X` | Delete the character before the cursor |
| `dd` | Delete the current line |
| `db` | Delete backward to the beginning of a word |
| `de` | Delete through the end of the current word |
| `dw` | Delete to the beginning of the next word |
| `d4w` | Delete across four word movements |
| `s` | Delete the character under the cursor and enter Insert mode |
| `S` | Delete the current line's text and enter Insert mode |
| `C` | Delete from the cursor to the end of the line and enter Insert mode |
| `r` | Replace the character under the cursor with the next typed character |

## Repeat and undo

| Command | Result |
| --- | --- |
| `.` | Repeat the last change |
| `u` | Undo the last change |
| `Ctrl-R` | Redo an undone change |

## Keep learning

Run `vimtutor` in a terminal for Vim's interactive tutorial. These external guides are also useful:

- [Shawn Biddle's Vim classes](https://github.com/shawncplus/vim-classes)
- [Class recording](https://youtu.be/Nim4_f5QUxA)
- [OpenVim tutorial](https://www.openvim.com/)
