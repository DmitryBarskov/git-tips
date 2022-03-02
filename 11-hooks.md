# Git Hooks

## WARNING: don't use server side hooks

Try not to use server-side git hooks, they usually annoy devs. But client-side
hooks are totally fine, because
[you can easily disable it](https://git-scm.com/docs/git-commit#Documentation/git-commit.txt---no-verify).

### quickhook

[dirk/quickhook](https://github.com/dirk/quickhook)
```bash
brew tap dirk/quickhook

brew install quickhook

mkdir -p .quickhook/pre-commit

cat bin/rubocop > .quickhoook/pre-commit/rubocop

quickhook install
```

Pros:
+ Fast

Cons:
- Needs separate installation
- No instructions for building on linux

### overcommit
[sds/overcommit](https://github.com/sds/overcommit)
```bash
bundle add overcommit --group development

bundle exec overcommit --install

echo 'gemfile: Gemfile' >> .overcommit.yml

# Or uncomment
echo 'PreCommit:
  RuboCop:
    enabled: true
    on_warn: fail' >> .overcommit.yml
```

Pros:
+ Easier to install automatically
+ Has many checks by default

Cons:
- Slow
