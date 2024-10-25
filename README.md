# config
configs, dotfiles, installation notes

these are all used when installing archlinux, but should work for any other distribution

## setting correct system locale for time, date and currency, while keeping english as the primary system language
i work with a lot of documents in serbian latin and cyrillic, so i like having my system set to the appropriate time and date notation, without changing the system language.

to do this, i run the following commands:

* uncomment relevant rs_RS UTF-8 locales from the `/etc/locale.gen` file
* `sudo locale-gen`
* `sudo localectl set-locale LANG=sr_RS.UTF-8 LC_MESSAGES=en_US.UTF-8` this sets the time and date notation to serbian cyrillic, which i personally prefer, and keeps the american english as default system language
* reboot
