---

### `dive/README.md`
```markdown
# dive 🐋

**dive** is a lightweight fuzzy finder helper that lets you quickly navigate into project directories and open them in [Neovim](https://neovim.io).

## How it works
- Uses `find` to recursively list directories (ignores `.git` folders).  
- Pipes the list into [fzf](https://github.com/junegunn/fzf) for interactive selection.  
- Opens the selected directory in Neovim.

---

## 1. Install Requirements
 

Arch Linux:

```bash
sudo pacman -S fzf neovim

Debian based:
```bash
sudo apt install fzf neovim

MacOS:
```bash
brew install fzf neovim

---

## 2. Install dive

```bash
git clone https://github.com/NikitaTLN/Dive.git
cd dive
chmod +x dive
mkdir -p ~/.local/bin/
mv dive ~/.local/bin/

---

## 3. Add to you PATH (optional)

Zsh:
```zsh
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc 
source ~/.zshrc

Bash:
```bash
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc 
source ~/.bashrc

---

## 4. Usage


```bash
dive


---

## 5. Keybinding (optional)

Zsh:

```zsh
nvim ~/.zshrc

# Add this line to the file:
bindkey -s 'YOURKEY' '~/.local/bin/dive\n'

# for example 

bindkey -s '^f' '~/.local/bin/dive\n'

Bash:

```bash
nvim ~/.bashrc

# Add this line to the file:

bind -x '"YOURKEY":"~/.local/bin/dive"'

# for example:

bind -x '"\C-f":"~/.local/bin/dive"'
