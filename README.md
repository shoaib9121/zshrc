# .zshrc
This file contains the various `.bashrc/.zshrc` scripts

# For vscode to open file/directory through `code` command
```
code () { VSCODE_CWD="$PWD" open -n -b "com.microsoft.VSCode" --args $* ;}
```
---

# Visual Customization Power Level Shell
Below are the scripts for custom shell based on theme `Powerlevel10k`

## Install Fonts
[MesloLGS NF Regular.ttf](https://github.com/romkatv/powerlevel10k#configuration-wizard:~:text=MesloLGS%20NF%20Regular.ttf)
[MesloLGS NF Bold.ttf](https://github.com/romkatv/powerlevel10k#configuration-wizard:~:text=MesloLGS%20NF%20Bold.ttf)
[MesloLGS NF Italic.ttf](https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Italic.ttf)
[MesloLGS NF Bold Italic.ttf](https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold%20Italic.ttf)

## Install `Oh My Zsh`

```
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

Below output should be displayed after install

<img width="1224" alt="ohmyzsh" src="https://github.com/shoaib9121/zshrc/assets/24590278/40d67c24-a2c3-4410-9714-c2516ea6968e">

## Powerlevel10k
```
git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
```

Paste `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc` file
run `source ~/.zshrc` (prompt wizard should appear)

If prompt wizard not appeared
run `p10k configure`

#### Reference
https://dev.to/abdfnx/oh-my-zsh-powerlevel10k-cool-terminal-1no0

https://www.swtestacademy.com/customize-mac-terminal/

---

## Install `nvm`
```
brew update
brew install nvm
```

Create a directory for NVM at home.
```
mkdir ~/.nvm
```

Add below snippet in ~/.zshrc
```
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
```
OR
```
export NVM_DIR="~/.nvm"
source $(brew --prefix nvm)/nvm.sh
```
