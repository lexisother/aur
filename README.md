# Alyxia's Arch Packages

This repository contains all sorts of packages, from my programs, edited AUR packages, and Discord plugins. Yes, I know, the last one sounds weird.

## Package Repository

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

## On the topic of `aurbuild`

I have made some updates to the script, and have added extra configuration options to the list of environment variables.

| Name                  | Description                                                                      | Required |
|-----------------------|----------------------------------------------------------------------------------|----------|
| `repository_location` | The *full path* of your repository.                                              | x        |
| `repository_name`     | The name of your repository.                                                     | x        |
| `auto_update`         | Whether to automatically run `repo-add` to add all packages to the repository.   |          |
| `auto_publish`        | Whether to automatically use `scp` to move your repository to a remote location. |          |
| `publish_location`    | The remote location of your repository. Must be a path.                          |          |
| `publish_port`        | The port used for SSH. By default 21.                                            |          |

## Credits

Entire repository including aurbuild shamelessly copied from [AVR](https://github.com/vbouchaud/aur).
