# Verified check on GitHub

0. Install gnupg `brew install gnupg`
0. Generate a new key `gpg --default-new-key-algo rsa4096 --gen-key`
0. Output key ID and remember it: `export KEY_ID="$(gpg --list-secret-keys --keyid-format LONG | head -3 | tail -1 | cut -c 15-30)"`
0. Export key `gpg --armor --export $KEY_ID`
0. Add it to GitHub https://github.com/settings/gpg/new
0. Configure git `git config --global user.signingkey $KEY_ID`
0. Create a signed off commit `git commit -S -m "Initial commit"`

I had some issues and this Stackoverflow answer helped me https://stackoverflow.com/a/47087248/14209416.

## Renew an expired key

Here is useful link [Renew expired GPG key (GitHub Gist)](https://gist.github.com/krisleech/760213ed287ea9da85521c7c9aac1df0).
