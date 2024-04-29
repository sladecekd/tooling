# SSH from Keychain

- Load the keys automatically `~/.ssh/config`

``` ssh
Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_ed25519
```

- Add the private-key

``` zsh
ssh-add --apple-use-keychain ~/.ssh/id_ed25519
```
