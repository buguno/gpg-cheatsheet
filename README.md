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

## :wastebasket: Delete key

```bash
# Remove key from the public keyring.
gpg --delete-keys <ID>

# Remove key from the secret keyring.
gpg --delete-secret-keys <ID>

# Same as --delete-key, but if a secret key exists, it will be removed first.
gpg --delete-secret-and-public-key <ID>
```

## :no_entry_sign: Revoke key

```bash
# Generate a revocation certificate for the complete key.
gpg --output <OUTPUT FILE NAME> --gen-revoke <ID>
```
