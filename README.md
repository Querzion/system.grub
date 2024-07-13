## system.grub
A repo for Grub, configs and themes.

# Installation
Copy the ex. "breeze" directory to a location GRUB can access it. The standard path is ```/usr/share/grub/themes/```, but if your installing this theme in an encrypted system, you might prefer to copy this package content to ```/boot``` and set your GRUB configuration file accordingly.
  - Edit the Grub config file:
```bash
sudo nano /etc/default/grub
```
  - making sure this line (or a variant of it) exists:
```bash
GRUB_THEME="/usr/share/grub/themes/breeze/theme.txt"
```
  - And then run:
```bash
sudo grub-mkconfig -o /boot/grub/grub.cfg
```
  - Do change 'breeze' with any other theme name that you wish to install.
