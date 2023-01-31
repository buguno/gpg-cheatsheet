# GPG cheatsheet

## :sparkles: Generate key

```bash
gpg --full-generate-key
```

## :clipboard: List keys

```bash
# List all keys
gpg --list-keys

# Private keys
gpg --list-secret-keys

# Public keys
gpg --list-public-keys

# List the long form of the GPG keys for which you have both a public and private key.
gpg --list-secret-keys --keyid-format=long

# List  all  keys  (or the specified ones) along with their fingerprints.
gpg --fingerprint
```
