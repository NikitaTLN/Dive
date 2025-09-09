---

### `dive/README.md`
```markdown
# dive 🐋

**dive** is a lightweight fuzzy finder helper that lets you quickly navigate into project directories and open them in [Neovim](https://neovim.io).

## How it works
- Uses `find` to recursively list directories (ignores `.git` folders).  
- Pipes the list into [fzf](https://github.com/junegunn/fzf) for interactive selection.  
- Opens the selected directory in Neovim.

