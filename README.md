# GPG cheatsheet

## :sparkles: Generate key

```bash
gpg --full-generate-key
```

## :clipboard: List keys

```bash
# List all keys
gpg --list-keys

# List secret keys
gpg --list-secret-keys

# List public keys
gpg --list-public-keys

# List the long form of the GPG keys for which you have both a public and private key.
gpg --list-secret-keys --keyid-format=long

# List all keys (or the specified ones) along with their fingerprints.
gpg --fingerprint
```

## :wastebasket: Delete keys

```bash
# Remove key from the public keyring.
gpg --delete-keys <NAME>

# Remove key from the secret keyring.
gpg --delete-secret-keys <NAME>

# Same as --delete-key, but if a secret key exists, it will be removed first.
gpg --delete-secret-and-public-key <NAME>
```
