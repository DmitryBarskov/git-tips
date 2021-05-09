# Adding co-authors to commits

To add a co-author to commit use

```bash
git commit -m "Address changes from code review

Co-authored-by: Arthur Zaharov <arthur.zaharov@flatstack.com>"
```

This will result in

![Co-authors in GitHub](images/co-authors.png)

I have a file `mates` that have variables with names with people I work with

```bash
export ARTHUR_ZAHAROV='Co-authored-by: Arthur Zaharov <arthur.zaharov@flatstack.com>'
```

So I commit using
```bash
git commit -m "Address changes from code review

$ARTHUR_ZAHAROV"
```
