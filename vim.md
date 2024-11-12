
# Mini Guide to Vim

Vim is a highly configurable text editor used for editing code and text. It’s known for its efficiency and versatility once you get used to its commands. Below is a quick guide to help you get started with Vim.

## 1. Starting Vim

To start Vim, simply type:

```bash
vim <filename>
```

If the file doesn't exist, Vim will create it when you save.

## 2. Vim Modes

Vim operates in several modes, the most important being:

- **Normal mode**: For navigation and editing.
- **Insert mode**: For text input.
- **Visual mode**: For selecting text.

### Switching Modes

- **Normal mode**: Press `Esc` to return to normal mode.
- **Insert mode**: Press `i` to enter insert mode (for typing).
- **Visual mode**: Press `v` to enter visual mode for selecting text.

## 3. Basic Navigation

- **Move the cursor**:
    - Arrow keys or `h` (left), `j` (down), `k` (up), `l` (right).
- **Move by word**: `w` (next word), `b` (previous word).
- **Move to the beginning of the line**: `0` (zero).
- **Move to the end of the line**: `$`.
- **Move to the next paragraph**: `{` or `}`.

## 4. Editing Text

- **Delete a character**: `x` (delete the character under the cursor).
- **Delete a line**: `dd` (delete the current line).
- **Undo changes**: `u` (undo the last action).
- **Redo changes**: `Ctrl + r` (redo the undone action).
- **Copy text**: `y` (yank, copy the selected text).
- **Paste text**: `p` (paste after the cursor), `P` (paste before the cursor).

## 5. Searching and Replacing

- **Search for a word**: `/word` (search forward), `?word` (search backward).
- **Repeat search**: Press `n` to repeat the search forward, `N` for backward.
- **Replace a word**: `:%s/old/new/g` (replace all occurrences of "old" with "new" in the file).
- **Replace with confirmation**: `:%s/old/new/gc` (replace with confirmation for each match).

## 6. Saving and Exiting

- **Save the file**: `:w` (write the file).
- **Exit Vim**: `:q` (quit Vim). If you haven’t saved changes, it will warn you.
- **Save and exit**: `:wq` (write and quit).
- **Force exit without saving**: `:q!` (quit without saving changes).
- **Exit if nothing to save**: `:x` (save and exit if there were any changes).

## 7. Working with Multiple Files

- **Open a file**: `vim <filename>` (open a specific file).
- **Switch between files**: `:n` (next file), `:prev` (previous file).
- **Close the current file**: `:bd` (close the current buffer).

## 8. Visual Mode

- **Select text**: Press `v` to start selecting characters, `V` for lines, or `Ctrl+v` for block selection.
- **Delete selected text**: Press `d` after selecting.
- **Copy selected text**: Press `y` after selecting.
- **Paste selected text**: Press `p` to paste.

## 9. Vim Tips and Tricks

- **Scroll by half-page**: `Ctrl + u` (up), `Ctrl + d` (down).
- **Split the window horizontally**: `:sp` (split window).
- **Split the window vertically**: `:vsp` (split window vertically).
- **Move between splits**: `Ctrl + w` followed by a direction key (`h`, `j`, `k`, `l`).
- **Show line numbers**: `:set number`.

## Conclusion

Vim can seem overwhelming at first, but once you get used to its commands and shortcuts, it becomes an incredibly powerful tool for editing code. Practice these basic commands, and soon you’ll be navigating and editing files like a pro.
