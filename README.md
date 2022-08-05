# .zshrc
This file contains the various `.bashrc/.zshrc` scripts

# Visual Customization Power Level Shell
Below are the scripts for custom shell based on theme `powerlevel9k/powerlevel9k`
```
ZSH_THEME="powerlevel9k/powerlevel9k"
POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(dir rbenv vcs)
POWERLEVEL9K_RIGHT_PROMPT_ELEMENTS=(status root_indicator background_jobs history time)
POWERLEVEL9K_PROMPT_ON_NEWLINE=true
```
#### Add a space in the first prompt 
```
POWERLEVEL9K_MULTILINE_FIRST_PROMPT_PREFIX="%f"
```
#### Visual customisation of the second prompt line
```
local user_symbol="$"
if [[ $(print -P "%#") =~ "#" ]]; then
    user_symbol = "#"
fi
POWERLEVEL9K_MULTILINE_LAST_PROMPT_PREFIX="%{%B%F{black}%K{yellow}%} $user_symbol%{%b%f%k%F{yellow}%} %{%f%}"
```
#### Change the git status to red when something isn't committed and pushed
```
POWERLEVEL9K_VCS_MODIFIED_BACKGROUND='red'
```
#### And finally give the path to theme
```
source /Users/[HOME_USER]/.oh-my-zsh/custom/themes/powerlevel9k/powerlevel9k.zsh-theme
```
