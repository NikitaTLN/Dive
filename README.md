## Dive 

dive - is a lightweight fuzzy finder helper that lets you quickly navigate into project directories and open them in [Neovim](https://neovim.io).

## How it works
- Uses `find` to recursively list directories (ignores `.git` folders).  
- Pipes the list into [fzf](https://github.com/junegunn/fzf) for interactive selection.  
- Opens the selected directory in Neovim.


## 1. Install Requirements
 

Arch Linux:

```bash
sudo pacman -S fzf neovim
```
Debian based:
```bash
sudo apt install fzf neovim
```
MacOS:
```bash
brew install fzf neovim
```
---

## 2. Install dive

```bash
git clone https://github.com/NikitaTLN/Dive.git
cd dive
chmod +x dive
mkdir -p ~/.local/scripts/
mv dive ~/.local/scripts/
```
---

## 3. Add to your PATH (optional)

Zsh:
```bash
echo 'export PATH="$HOME/.local/scripts:$PATH"' >> ~/.zshrc 
source ~/.zshrc
```
Bash:
```bash
echo 'export PATH="$HOME/.local/scripts:$PATH"' >> ~/.bashrc 
source ~/.bashrc
```
---

## 4. Usage


```bash
dive
```

---

## 5. Keybinding (optional)

# Zsh:

```bash
echo "bindkey -s 'YOURKEY' '~/.local/scripts/dive\n'" >> ~/.zshrc
```

for example:

```bash
echo "bindkey -s '^f' '~/.local/scripts/dive\n'" >> ~/.zshrc
# bind ctrl+f to run dive
```

# Bash:

```bash
echo "bind -x '"YOURKEY":"~/.local/scripts/dive"'" >> ~/.bashrc
```

for example:

```bash
echo "bind -x '"\C-f":"~/.local/scripts/dive"'" >> ~/.bashrc
# bind ctrl+f to run dive
```
