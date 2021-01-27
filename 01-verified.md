0. Install gnupg `brew install gnupg`
0. Generate a new key `gpg --default-new-key-algo rsa4096 --gen-key`
0. Output key ID and remember it: `export KEY_ID="$(gpg --list-secret-keys --keyid-format LONG | head -3 | tail -1 | cut -c 15-30)"`
0. Export key `gpg --armor --export $KEY_ID`
0. Add it to GitHub https://github.com/settings/gpg/new
0. Configure git `git config --global user.signingkey $KEY_ID`
