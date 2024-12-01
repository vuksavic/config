# config
configs, dotfiles, installation notes

these are all used when installing arch linux

## install yay
* `sudo pacman -S --needed git base-devel`
* `git clone https://aur.archlinux.org/yay-bin.git`
* `cd yay-bin`
* `makepkg -si`
* `yay -Y --gendb`

## setting correct system locale for time, date and currency, while keeping english as the primary system language
i work with a lot of documents in serbian latin and cyrillic, so i like having my system set to the appropriate time, date and currency notation, without changing the system language.

to do this, run the following commands:

* uncomment relevant rs_RS UTF-8 locales from the `/etc/locale.gen` file
* `sudo locale-gen`
* `sudo localectl set-locale LANG=sr_RS.UTF-8 LC_MESSAGES=en_US.UTF-8` this sets the time and date notation to serbian cyrillic, which i personally prefer, and keeps the american english as default system language
* reboot

## installing blackarch repo
i'm going through some hackthebox courses to get into network security, so it's nice to have some of those tools locally on my machine. for arch linux, there's the blackarch repo from the blackarch distro.

* `curl -O https://blackarch.org/strap.sh`
* `chmod +x strap.sh`
* `sudo ./strap.sh`
* `sudo pacman -Syu` or just `yay`
