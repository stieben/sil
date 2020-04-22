# Working with GPG keys

_#unix_ _#bash_ _#gpg_

## List all keys currently registered

```bash
$ gpg2 --list-keys --keyid-format LONG
/home/alice/.gnupg/pubring.kbx
-------------------------------
pub   rsa4096/7AC891336421B3D4 2020-01-02 [SC] [expires: 2024-01-01]
      0FD09AA324DB8FA0D11615D7744AA1311421A311
uid               Alice <alice@wonderland.net>
sub   rsa4096/B4A9B1530AADA321 2020-01-02 [E] [expires: 2024-01-01]
```

## Export public key

Choose one of these:

```bash
$ gpg2 --output alice.pub --armor --export 7AC891336421B3D4
$ gpg2 --output alice.pub --armor --export alice@wonderland.net
```

## Import public key

```bash
$ gpg2 --import bob.pub
```

## Sources

- [GitHub Help](https://help.github.com/en/github/authenticating-to-github/generating-a-new-gpg-key)
- [The GNU Privacy Handbook](https://www.gnupg.org/gph/en/manual/x56.html)
