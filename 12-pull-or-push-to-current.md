# Pull/push from/to current branch

1. Bash alias

```bash
alias gpull='git pull origin $(git branch --show-current)'
```

2. Git alias

```gitconfig
[alias]
  pc = !git pull origin $(git branch --show-current)
```

3. The Fuck

```bash
$ git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> br-1

$ fuck
git branch --set-upstream-to=origin/br-1 br-1 && git pull [enter/↑/↓/ctrl+c]
Branch 'br-1' set up to track remote branch 'br-1' from 'origin'.
Already up to date.
$ git pull
Already up to date.
```

4. Set upstream + config

The config
```gitconfig
[push]
  default = current
[alias]
  pu = push -u
```
