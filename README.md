# GPG cheat sheet

gpg is the OpenPGP part of the GNU Privacy Guard (GnuPG). It is a tool to provide digital encryption and signing services using the OpenPGP standard. gpg features complete key management and all the  bells  and whistles you would expect from a full OpenPGP implementation.
The repository is for quick queries of the most used commands.

## Summary

1. [:sparkles: Generate key](#sparkles-generate-key)
2. [:clipboard: List keys](#wastebasket-delete-key)
3. [:wastebasket: Delete key](#wastebasket-delete-key)
4. [:no_entry_sign: Revoke key](#no_entry_sign-revoke-key)
5. [:outbox_tray: Export key](#outbox_tray-export-key)
6. [:inbox_tray: Import key](#inbox_tray-import-key)
7. [:lock_with_ink_pen: Signatures](#lock_with_ink_pen-signatures)
8. [:lock: Encrypt](#lock-encrypt)

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

## :outbox_tray: Export key

```bash
# Export public key and save in a file
gpg --output <OUTPUT FILE NAME> --export --armor <ID>

# Export secret key and save in a file
gpg --output <OUTPUT FILE NAME> --export-secret-keys --armor <ID>
```

## :inbox_tray: Import key

```bash
# Import a key
gpg --import <FILE>
```

## :lock_with_ink_pen: Signatures

```bash
# Sign data
gpg --sign <FILE>

# Make a cleartext signature
gpg --clear-sign <FILE>

# Sign data with a specific key
gpg --default-key <ID> --sign <FILE>

# Create a detached signature
gpg --detach-sign <FILE>

# Verify the signature
gpg --verify <FILE>

# or
gpg --verify <FILE>.sig <FILE>
```

## :lock: Encrypt

```bash
# Encrypt symmetric
gpg --symmetric <FILE>

# Encrypt asymmetric
gpg --encrypt <FILE>

# Encrypt asymmetric and set the receiver
gpg --encrypt --recipient <RECEIVER ID> <FILE>

# Encrypt and sign
gpg --encrypt --sign <FILE>
```
