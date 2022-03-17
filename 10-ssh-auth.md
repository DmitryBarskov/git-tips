# SSH authentication in GitHub

[Original instruction](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

1. Generate SSH key
```bash
ssh-keygen
```

Select file location, passphrase (I prefer empty)

2. Copy the key
```bash
cat "$HOME/.ssh/id_rsa.pub" | pbcopy
```

3. Visit [GitHub Settings](https://github.com/settings/ssh/new) and add the key
Example:
```
Title:
Personal Macbook Air 2015

Key:
ssh-rsa AAA...JaE= dmitry.barskov@flatstack.com
```
4. Replace HTTPS remotes with SSH
```bash
git remote remove origin
git remote add origin git@github.com:fs/rails-base-graphql-api.git
```

Pros:
1. Secure
2. Don't need to log in every time
