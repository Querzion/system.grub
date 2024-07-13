## system.grub
A repo for Grub, configs and themes. The visuals beneeth is more or less directly copied from "https://github.com/Jacksaur/Gorgeous-GRUB"

# 🛠️ Installation

GRUB themes are all installed the same way. Some themes may provide an install script, feel free to use it if you want, it should just take the same actions described here. Some theme pages recommend using **GRUB Customizer**, I do not. It changes your GRUB config files and can make it difficult to apply tweaks or changes.

Click the title of the Theme you want to install and you should be taken to its page: Either on Pling or Github. Pling will have a Files tab right below the preview screenshot, Github should have a green CODE button you can click to clone the repo. Some themes are stored in folders of a larger repo, if you copy the URL and paste it into Gitzip (Check the Useful Links section) you can download just those files, rather than cloning the entire repo.

Once you have the theme files, it's just a simple matter of dropping them into a folder in ```/boot/grub/themes```. You may need to change the owner of this folder to interact with it, using the command ```sudo chown $USER /boot/grub/themes```. You should now have a folder in the themes directory named after the theme, and that folder should include the theme.txt and any other relevant files that theme came with.

Once the theme is in place, you just need to set GRUB to use it. Navigate to ```/etc/default``` and edit the grub file in there. You'll require Root permissions for this, you can use the sudoedit command to easily open it in your terminal. It's not a difficult edit either way, you won't need to use the terminal editor for long. Find the ```GRUB_THEME=``` line and add the path to the theme.txt of the theme you want to use. Don't forget to change the ```#GRUB_GFXMODE=``` line to your desired resolution, removing the # to enable it.
Finally, run the command ```sudo update-grub``` to finalize your changes. You need to run this command every time you make changes to a config file. (If you're on Fedora, the command is ```sudo grub2-mkconfig -o /boot/grub2/grub.cfg``` instead)

Upon restart, you should find your new theme will be used for your bootloader!

# 🚀 Customization Tips
There are many great community made GRUB themes to spice up your bootloader before booting into your system proper. Unfortunately, they're spread across multiple sites and it can be difficult to find good ones. As another user told me, the majority of themes on Pling (the largest host of GRUB themes currently) are fairly low effort and can be boring to trawl through. Hence, I decided to put together this page to bring attention to some decent themes I've found around the internet over time. They aren't all absolute masterpieces of course: But they've all at least had a fair amount of effort put into them, with custom backgrounds, fonts, and colours.  

And don't forget, **themes are extremely easy to customize!** Like a theme's layout but prefer a different background? Just replace the image in its folder with one of your own. Don't like the positioning of a theme's elements? Open the theme.txt and change their values. Want a different colour scheme? They're all set by HEX Values, which you can swap out in seconds. You can even convert almost any font to the type GRUB uses with the grub-mkfont command, then change the `item_font` line in the theme.txt to use it.  
There's loads of potential for customization, you just have to work creatively around the limitations.

# 🌟 Useful Links

[GitZip](https://kinolien.github.io/gitzip/) - Download individual folders and files from Github repositories without having to download the entire repo. Asks for a Token, but seems to work without just fine.  

[GRUB-Tweaks](https://github.com/VandalByte/grub-tweaks) - Multiple guides on various tweaks and additions you can make to further customize, or repair, your GRUB install.  

[Theme Tutorial](http://wiki.rosalab.ru/en/index.php/Grub2_theme_tutorial) and [Theme References](http://wiki.rosalab.ru/en/index.php/Grub2_theme_/_reference) - Pretty complex, but the best set of information I've managed to find so far. It may be easier to start by taking an existing theme and making edits to it yourself, rather than diving straight in and starting from scratch.  

[Background Cycler](https://github.com/Jacksaur/GRUB-Background-Cycler) - Script I (Jacksaur) made that will cycle a theme to a different background each time your system is rebooted. The Cron job can be modified to run at specific amounts of time instead if desired.

# 👍 Contributing
Contributions are very welcome, either of themes you've created yourself or just ones you've discovered online. Just open a Pull Request and it to the Table with a preview image and link to the page where the theme is hosted.
If you're not sure how, just open an Issue with the link and preview image included, and I'll add it myself when I get the chance.

Bear in mind, there are a few rules on what will be accepted:

  - The majority of elements must be changed from default: Themes that consist of the default GRUB menu with just a background thrown in will not be accepted. In the least please try to include a custom background, menu selector and flavor text.
  - Forks of existing themes must be recognizably different from their original: Altering an existing theme is an excellent way to learn without having to read through GRUB's sparse documentation. But if you wish to share an edited theme here, please ensure you've changed enough of it to stand out against the original. This page was created to make it easier to find unique themes, and that falls apart if every theme is a vague alteration to an existing one. Compare my CRT-Amber theme to the Fallout theme that it's forked from, for an example of how different it should be.
  - Theme must not be too similar to ones already on the page: Similar to above, but even for completely custom themes. Though if your theme is significantly higher quality than the one it's similar to, it may be possible to replace the former.
  - No Waifu themes: Anime related themes are fine, but please, no themes revolving entirely around generic renders of an anime character. Pling has hundreds of these in every category, not just GRUB. Again, Anime is fine, this is just a rule against themes that consist of a few fancy colours and a single cutout of an anime character.
  - SFW only: You'd think this is obvious, but you'd be surprised! 😳

# 🎨 Themes

>If you like a theme, please do consider giving it a rating on Pling or starring its repo on Github. It's very rare for anyone to rate on Pling and that's half the reason good themes are so hard to find. Plus, it always feels nice to see that people are enjoying the product you created.

|    |    |    |
|:-------:|:-------:|:---------:|
|<img src="/Images/Minegrub.png" width="247">|<img src="/Images/Descent.jpg" width="247">|<img src="/Images/SteamOS.png" width="247">|
|**[Minegrub (Cycling Text)](https://github.com/Lxtharia/minegrub-theme) + [Combined Version!](https://github.com/Lxtharia/double-minegrub-menu)**|[**Descent**](https://www.pling.com/p/1000083/)|[**SteamOS (Personalized)**](https://github.com/LegendaryBibo/Steam-Big-Picture-Grub-Theme)|
|    |    |    |
|<img src="/Images/Virtuaverse.png" width="247">|<img src="/Images/Yorha.png" width="247">|<img src="/Images/CRT-Amber.png" width="247">|
|[**Virtuaverse**](https://github.com/Patato777/dotfiles/tree/main/grub)|[**YoRHa**](https://github.com/OliveThePuffin/yorha-grub-theme)|[**CRT-Amber**](https://www.pling.com/p/1727268/)|
|    |    |    |
|<img src="/Images/Minegrub-World.png" width="247">|<img src="/Images/Dedsec.gif" width="247">|<img src="/Images/Sekiro.png" width="247">|
|**[Minegrub World Select](https://github.com/Lxtharia/minegrub-world-sel-theme) + [Combined Version!](https://github.com/Lxtharia/double-minegrub-menu)**|[**DedSec (Set)**](https://www.pling.com/p/1569525/)|[**Sekiro**](https://github.com/semimqmo/sekiro_grub_theme)|
|    |    |    |
|<img src="/Images/HyperFluent.gif" width="247">|<img src="/Images/Persona5.gif" width="247">|<img src="/Images/Graphite.png" width="247">|
|[**HyperFluent (Set)**](https://www.pling.com/p/2133341/)|[**Persona 5 Royal (Set)**](https://www.pling.com/p/2122684)|[**Graphite**](https://www.pling.com/p/1676418/)|
|    |    |    |
|<img src="/Images/Linux_Mind.png" width="247">|<img src="/Images/Fallout.png" width="247">|<img src="/Images/CyberEXS.png" width="247">|
|[**Linux Mind**](https://www.pling.com/p/1397139/)|[**Fallout**](https://www.pling.com/p/1230882/)|[**CyberEXS**](https://www.pling.com/p/1968990)|
|    |    |    |
|<img src="/Images/Cyberpunk2077.png" width="247">|<img src="/Images/CyberRe.png" width="247">|<img src="/Images/Cyberpunk.png" width="247">|
|[**Cyberpunk 2077**](https://www.pling.com/p/1515662/)|[**CyberRe**](https://www.pling.com/p/1420727/)|[**Cyberpunk**](https://www.pling.com/p/1429443/)|
|    |    |    |
|<img src="/Images/Framework.png" width="247">|<img src="/Images/Sayonara.png" width="247">|<img src="/Images/LiteMint.png" width="247">|
|[**Framework**](https://github.com/HeinrichZurHorstMeyer/Framework-Grub-Theme)|**[Sayonara](https://github.com/samoht9277/dotfiles/tree/55455eec2c2df83be5373b1095915bb7086b1dab/grub/themes/sayonara) + [Improved Font](https://www.dropbox.com/s/il0dxjq5u65t0pt/Font.zip?dl=0)**|[**Neumorphic**](https://www.pling.com/p/1906415)|
|    |    |    |
|<img src="/Images/OldBIOS.png" width="247">|<img src="/Images/Arcade.png" width="247">|<img src="/Images/DOOM.png" width="247">|
|[**OldBIOS**](https://www.pling.com/p/2072033)|[**Arcade**](https://github.com/nobreDaniel/dotfile)|[**DOOM**](https://github.com/Lxtharia/doomgrub-theme)|
|    |    |    |
|<img src="/Images/Dark_Matter.gif" width="247">|<img src="/Images/Aero.png" width="247">|<img src="/Images/Sleek.gif" width="247">|
|[**Dark Matter (Set)**](https://www.pling.com/p/1603282/)|[**Aero**](https://www.pling.com/p/1112066/)|[**Sleek (Set + Personalized)**](https://www.pling.com/p/1414997/)|
|    |    |    |
|<img src="/Images/Standby.png" width="247">|<img src="/Images/Axiom.jpg" width="247">|<img src="/Images/Solarized-Dark.png" width="247">|
|[**Standby**](https://www.pling.com/p/1172610/)|[**Axiom**](https://www.pling.com/p/1111735/)|[**Solarized-Dark**](https://www.pling.com/p/1177401/)|
|    |    |    |
|<img src="/Images/Retro_GRUB.png" width="247">|<img src="/Images/BigSur.png" width="247">|<img src="/Images/Distro.gif" width="247">|
|[**Retro GRUB**](https://www.pling.com/p/1568741/)|[**BigSur**](https://www.pling.com/p/1443844/)|[**Distro Themes (Set)**](https://www.pling.com/p/1482847/)|
|    |    |    |
|<img src="/Images/Poly.gif" width="247">|<img src="/Images/Atomic.png" width="247">|<img src="/Images/Plasma.gif" width="247">|
|**Poly ([Light](https://www.pling.com/p/1176413/)/[Dark](https://www.pling.com/p/1230780/))**|[**Atomic**](https://www.pling.com/p/1200710/)|**Plasma ([Light](https://www.pling.com/p/1197062/)/[Dark](https://www.pling.com/p/1195799/))**|
|    |    |    |
|<img src="/Images/Solstice.jpg" width="247">|<img src="/Images/Virtual_Future.png" width="247">|<img src="/Images/Grubby_Terminal.jpg" width="247">|
|[**Solstice**](https://www.pling.com/p/1111874/)|[**Virtual Future**](https://www.pling.com/p/1529571/)|[**Grubby Terminal**](https://gitlab.com/perthshiretim/grubby-terminal)|
|    |    |    |
|<img src="/Images/Billys_Agent.png" width="247">|<img src="/Images/Matter.gif" width="247">|<img src="/Images/Modern.gif" width="247">|
|[**Billy's Agent**](https://gitlab.com/Drorago/billys-agent-grub2-theme)|[**Matter (Customizable)**](https://www.pling.com/p/1400298/)|[**Modern Design Themes (Set)**](https://github.com/vinceliuice/grub2-themes)|
|    |    |    |
|<img src="/Images/Deadora.png" width="247">|<img src="/Images/Breeze.png" width="247">|<img src="/Images/GutsBlack-ArchLinux.png" width="247">|
|[**Deadora**](https://www.pling.com/p/1111550/)|[**Breeze**](https://www.pling.com/p/1000111/)|[**Gutsblack Archlinux**](https://forums.archlinux.fr/viewtopic.php?t=11361)|
|<img src="/Images/CyberXero.png" width="247">|<img src="/Images/Placeholder.png" width="247">|<img src="/Images/Placeholder.png" width="247">|
|[**CyberXero**](https://www.pling.com/p/1502415/)|-|-|

