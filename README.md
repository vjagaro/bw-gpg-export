# `bw-gpg-export`

## Usage

```
$ ./bw-gpg-export
This is a simple tool to make it easy to export your Bitwarden vault and
encrypt it with GnuPG symmetric encryption. This will not store any
unencrypted data on disk.

You will need your Bitwarden API key (client_id and client_secret). It can
be found in your web vault (https://vault.bitwarden.com/) by going to:
Settings / My Account / API Key.

client_id: user.11223344-5566-7788-99aa-bbccddeeff00
client_secret: S8M8fJq5scB17pKY1y0o9iQ8ErWbPp

Unlocking vault for me@domain.com...

Enter your master password [no echo]:

Select an organization to export:

0. No organization (your account)
1. Acme Incorporated
2. Bismuth Family

Choose (0-1): 1

25 items will be exported to a GnuPG symmetric encrypted file.

Enter export password [no echo]:
             again... [no echo]:

Exporting vault to: bitwarden-export-20220423-171901.json.gpg

To verify: gpg -qd bitwarden-export-20220423-171901.json.gpg | less

Your vault is locked.
```

## Install

This script depends on
[Bitwarden CLI](https://github.com/bitwarden/cli), [GnuPG](https://gnupg.org/) and
[jq](https://stedolan.github.io/jq/).

```sh
sudo snap install bw
sudo apt install -y gnupg jq
wget https://raw.githubusercontent.com/vjagaro/bw-gpg-export/main/bw-gpg-export
chmod +ax bw-gpg-export
```
