# Git completion

## For bash users

```bash
brew install bash-completion
echo '[[ -r "/usr/local/etc/profile.d/bash_completion.sh" ]]
  && . "/usr/local/etc/profile.d/bash_completion.sh"' >> .bash_profile
```

Use it
```bash
git checkout *word*
```

## For zsh users

```zsh
echo 'autoload -Uz compinit && compinit
autoload -Uz vcs_info' >> .zshrc
```

It will suggest all git commands, branch names.
