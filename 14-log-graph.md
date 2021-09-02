# git-log with graph option

Display history in rich format.
```bash
git log --graph
```

Don't try to learn format, just use this:
```gitconfig
  gr = log --graph --pretty=format:\"%Cred%h %Cblue%ar%Creset %Cgreen%an%Creset %s %Cred%d\"
  lg1 = log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all
  lg2 = log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold cyan)%aD%C(reset) %C(bold green)(%ar)%C(reset)%C(bold yellow)%d%C(reset)%n''          %C(white)%s%C(reset) %C(dim white)- %an%C(reset)' --all
```
