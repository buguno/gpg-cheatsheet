# GPG cheatsheet

## :sparkles: Generate key

```bash
gpg --full-generate-key
```

## List keys

```bash
# Private keys
gpg --list-secret-keys

# Public keys
gpg --list-public-keys

# List the long form of the GPG keys for which you have both a public and private key.
gpg --list-secret-keys --keyid-format=long
```
