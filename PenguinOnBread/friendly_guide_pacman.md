# A Friendly Guide for Pacman
## Update Mirror
### reflector
- reflector --country US --latest --sort rate --save /etc/pacman.d/mirrorlist
## Install a package
- sudo pacman -S zsh # install zsh package
- sudo pacman -Syu # S for Sync, y for update database (yy to force it), u for update package
- sudo pacman -Rns # R for Remove, n for remove unneeded config files, s for remove unneeded dependencies
- sudo pacman -Ss zsh # search package for zsh
- pacman -Q # query all installed package
- pacman -Qs zsh # search for package
- pacman -Qq # list all package with format for migration
- pacman -Qi zsh # display infomation for a package
- pacman -Q | wc -l # show how many package is installed
- pacman -Qe | wc -l # show how many package is explicitly installed
- pacman -Ql zsh # show the list of files in the package
- pacman -Qdt # list unrequired dependencies
- pacman -Qqdt | sudo pacman -Rns - # remove all unrequired dependencies quietly
- pacman -Scc # remove all cache
## config file
- path: /etc/pacman.conf
## downgrade
- use downgrade in AUR
- in a folder that contains PKGBUILD, use makepkg -Si to install the AUR package
## file lock
- path: /var/lib/pacman/db.lck
