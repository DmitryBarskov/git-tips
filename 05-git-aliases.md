# Git aliases

```bash
git config --global alias.co checkout
```

You should use __git__ aliases instead of your shell aliases to have
autocompletion on them.


```bash
$ git co some-br<t>
$ git co some-branch-name
```

You can use `!` to execute non git command

```bash
$ git config alias.sayHello '!echo hello'
$ git sayHello
> hello
```

Here is my alias section in git config

```gitconfig
[alias]
  a = add
  ad = add
  br = branch
  ci = commit -S
  co = checkout
  cob = checkout -b
  com = checkout master
  codestyle = commit -S -m 'Address code style offences'
  cp = cherry-pick
  dc = diff --cached
  df = diff
  f = fetch --all --prune
  p = pull
  pu = push -u
  s = status --short
  st = status
  unstage = restore --staged
```
