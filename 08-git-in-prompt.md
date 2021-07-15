# Show current branch in prompt

1. Check out this repo [bash-git-prompt](https://github.com/magicmonty/bash-git-prompt).

```bash
brew install bash-git-prompt

# Add next lines to your config file
[ -f "$(brew --prefix)/opt/bash-git-prompt/share/gitprompt.sh" ]; then
  __GIT_PROMPT_DIR=$(brew --prefix)/opt/bash-git-prompt/share
  GIT_PROMPT_ONLY_IN_REPO=1
  source "$(brew --prefix)/opt/bash-git-prompt/share/gitprompt.sh"
fi
```

2. My PS1
```bash
wget 'https://raw.githubusercontent.com/git/git/master/contrib/completion/git-prompt.sh'

# Or whereever you store git-prompt.sh file
if [ -f "$XDG_CONFIG_HOME/git/git-prompt.sh" ]; then
  source "$XDG_CONFIG_HOME/git/git-prompt.sh"
  export PS1="\[\033[34m\]\w\[\033[00m\]\[\033[31m\]\$(__git_ps1 ' %s')\[\033[00m\] $ "
else
  export PS1="\[\033[34m\]\w\[\033[00m\]\[\033[31m\] $ "
fi
```
