# Alyxia's Arch Packages

This repository contains all sorts of packages, from my programs, edited AUR packages, and Discord plugins. Yes, I know, the last one sounds weird.

## AVR Package Repository

To use the repo, first add [my GPG key](https://pgp.mit.edu/pks/lookup?op=get&search=0x355968D14144B739) to your Pacman keyring:

```sh
pacman-key --recv-keys 355968D14144B739
pacman-key --lsign-key 355968D14144B739
```
Note if you have trouble with your default key servers not being reachable try adding `--keyserver keyserver.ubuntu.com` to the first command.

Then add the following repository configuration to your `pacman.conf` after the *[community]* repository.

```ini
[alypkg]
Server = https://tobedecid.ed/$repo/$arch
```

## Credits

Entire repository including aurbuild shamelessly copied from [AVR](https://github.com/vbouchaud/aur).
