# Arch-Linux-Tips

This Repo includes tips and commands usefull for arch-linux-repo users. 
I will place any issue, command and tip which is usefull for myself here, Hope it will be usefull for any other user.

## Free space

#### Clean package cache:

The package cache is used to keep a record of packages that have been installed or upgraded. Over time, this cache can grow and take up a significant amount of space. You can clear the package cache by running the following command:
```bash
sudo pacman -Scc
```
This will remove all cached packages from your system.

#### Remove unused packages:
Over time, you may have installed packages that you no longer need. You can remove these packages using the following command:
```bash
sudo pacman -Rs $(pacman -Qtdq)
```
This will remove any packages that are no longer needed by your system.

#### Remove old journal files:
Arch Linux uses the systemd journal for logging. Over time, the journal files can take up a significant amount of space. You can remove old journal files using the following command:
```bash
sudo journalctl --vacuum-size=100M
```
This will remove any journal files that are larger than 100MB.

#### Clean up orphaned packages and dependencies:
Orphaned packages are packages that were installed as dependencies but are no longer needed by any other package. You can remove orphaned packages and their dependencies using the following command:
```bash
sudo pacman -Rns $(pacman -Qtdq)
```
This will remove any orphaned packages and their dependencies from your system.

#### Clean up your home directory:
Over time, your home directory can accumulate a lot of unnecessary files. You can clean up your home directory using the following command:
```bash
du -sh ~/* | sort -hr
```
This will show you the largest directories in your home directory. You can then remove any unnecessary files or directories to free up space.
