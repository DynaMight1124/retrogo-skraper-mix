# Small edit for RetroGo. All the hard work goes to EBZero and Tobio.

# RG Nano Skraper Mix
## Inspired by and forked from [garlic-onion-skraper-mix](https://github.com/ebzero/garlic-onion-skraper-mix) by **[EBZero](https://github.com/ebzero)**!
### Optimimized with (🧨) for tiny devices
#### It has come to my attention that Anbernic's OS contains components that have been used without permission from, or attribution to, the creators and developers. That being said I **very strongly** urge you to consider alternatives such as [this great project](https://github.com/DrUm78/FunKey-OS/releases/tag/FunKey-OS-DrUm78) which is built from [FunKey OS](https://github.com/FunKey-Project/FunKey-OS) and made for the Nano. By switching, you will gain many benefits such as:
- better user experience (no more forced boot into the clock)
- 60 FPS performance
- removal of sceen tearing issues
- better battery usage and overall performance
- [rich ecosystem of apps and games](https://wiki.funkey-project.com/wiki/List_of_third-party_OPK_applications)
- [welcoming community](https://discord.gg/NUzDGHQk) providing their expertise and time
- Plus much more

## Introduction
If you've ever tried to generate media for your game collection on the RG Nano, you may have been shocked when you saw the results. This pretty much summs up the experience:

![What's this? A game list for ANTS?!?](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/gamelist-for-ants.jpg)

Use this mix to generate media (example below) for your RG Nano. The game logos are scaled so they are easier to read and overlayed on a screen-shot. Generally works well for most of the themes included with the device.

## Sample Output
Here is some sample output created by the RG Nano Skraper Mix:

|                                       |                                       |                                       |
|:-------------------------------------:|:-------------------------------------:|:-------------------------------------:|
|![Kirby's Dream Land 2](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/kirbys-dream-land-2.jpg "Kirby's Dream Land 2")|![Harvest Moon](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/harvest-moon.jpg "Harvest Moon")|![Streets of Rage 2](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/streets-of-rage-2.jpg "Streets of Rage 2")|
|![Earthbound](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/earthbound.jpg "Earthbound")|![Duck Tales](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/duck-tales.jpg "Duck Tales")|![Fantastic Night Dreams Cotton](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/fantastic-night-dreams-cotton.jpg "Fantastic Night Dreams Cotton")|

## How to Use

### Stage 1 - Scrape Your Media with the Template Using Skraper
Generally, you want to follow the **[excellent instructions](https://github.com/ebzero/garlic-onion-skraper-mix#garlic-onion-skraper-mix)** created by [EB Zero](https://github.com/ebzero) and simply select the RG Nano XML template rather than the one made for Garlic/Onion devices.

Here is what's different from the original instructions. This all on the *Media* tab:
- **Output folder** should be set to **`%ROMROOTFOLDER%`**.
- **Gamelist Link** should be set to *No Link. Store one media per game/rom*.

A sample of the above settings is as shown:
![Sample Skraper Settings for Media Tab](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/sample-skraper-settings.png)

### Stage 2 - Convert PNGs to JPGs w/ optional Clean-Up (Not Required)
#### Note: This stage is **completely optional**. It will reduce the file size and should be (in theory) slightly more efficient on the limited hardware provided. Once again, **this is optional** and comes down to personal preference.

The **[PowerShell script](https://github.com/tobio-tenma/rg-nano-skraper-mix/blob/main/New-JpgsFromSkraper.ps1) creates JPG images from Skraper's PNG images. There is functinoality built-in to optionally purge the PNG files as after each successful JPG creation.

#### Quickstart
- Open a [Terminal](https://www.howtogeek.com/831728/7-ways-to-open-windows-terminal-on-windows-11/) at the location of the provided PowerShell script.
- Call the script as shown below in *Example 1* substituting "**`E:\`**" with the correct drive as according to your system.
  - Alternatively, provide the directory containing the scraped systems.
- *If you do not know the correct drive, open **File Explorer** and check **This PC** for the correct drive.*


##### Example 1 - Preserve Originals
Creates JPGs from the PNG files. No cleanup is performed:
```
.\New-JpgsFromSkraper.ps1 "E:\"
```
Note: The "E:\" could be different depending on your system configuration. Please double check to avoid issues.

##### Example 2 - Purge Originals
Creates JPGs from the PNG files. Cleans up by deleting PNGs successfully converted to JPG through the optional ``$true`` argument :
```
.\New-JpgsFromSkraper.ps1 "E:\" $true
```
Note: The "E:\" could be different depending on your system configuration. Please double check to avoid issues.

#### Conclusion
After running the script, your RG Nano / micro SD card can be safely ejected and removed and placed back into device.

## Screenshots
### FunKey OS
#### Coming soon...

### Anbernic's OS
Below are screenshots taken from each of the 11 themes provided by Anbernic:

|                                       |                                       |                                       |                                       |
|:-------------------------------------:|:-------------------------------------:|:-------------------------------------:|:-------------------------------------:|
| Classic                               | Fusion                                | Flat                                  | TFT                                   |
| ![Classic](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/Classic.png "Classic") | ![Fusion](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/Fusion.png "Fusion")| ![Flat](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/Flat.png "Flat") | ![TFT](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/TFT.png "TFT") |
| Marblewave                            | Nebula                                | Neon                                  | Pixxel                                |
| ![Marblewave](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/Marblewave.png "Marblewave") | ![Nebula](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/Nebula.png "Nebula") | ![Neon](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/Neon.png "Neon") | ![Pixxel](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/Pixxel.png "Pixxel")  |
| RetroRoomCovers                       | Sweetch                               | Anbernic                              | Bonus Kitty                           |
| ![RetroRoomCovers](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/RetroRoomCovers.png "RetroRoomCovers") | ![Sweetch](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/Sweetch.png "Sweetch")|![Anbernic](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/Anbernic.png "Anbernic") | ![Bonus Kitty](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/bonus-kitty.png "Bonus Kitty") |

## Real World Example
Here is what it should like when it's all said and done:

|                                       |                                       |                                       |
|:-------------------------------------:|:-------------------------------------:|:-------------------------------------:|
|![Sample 1](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/sample-1.jpg "Sample 1")|![Sample 2](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/sample-2.jpg "Sample 2")|![Sample 3](https://github.com/tobio-tenma/files/blob/main/RG-Nano-Scraper-Mix/sample-3.jpg "Sample 3")|

## Acknowledgements
**HUGE** thanks to **[ebzero](https://github.com/ebzero)** for the original [garlic-onion-skraper-mix](https://github.com/ebzero/garlic-onion-skraper-mix). It was viewing his work that inspired the transformation for the RG Nano! Consider giving a high-five, buying a coffee, or simply giving a shout out for making the code available for all to the benefit all. Also a huge shout out goes to DynaMight for meticulously optimizing and enhancing the image dimensions and coposition of the elements. Thanks to [DrUm78](https://github.com/DrUm78) for his [awesome distrobution](https://github.com/DrUm78/FunKey-OS/releases/tag/FunKey-OS-DrUm78) made for RG Nanos. Thank you to the [FunKey OS Project](https://github.com/FunKey-Project/FunKey-OS) who have been nothing but helpful and welcoming. Thanks to the theme developers for providing the user experience. Finally thanks to the whole community for being inclusive, collaberative, and just awesome in general.
