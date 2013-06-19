Introduction
============

This repository hosts all my Mudlet script packages for the mud Materia Magica. For information how to install Mudlet script packages, [see the Installation Instructions](#installation). Each script package has a description and dependencies(which other packages are needed) in the [List of Packages](#list-of-packages). The script packages are generally tested on Mudlet 2.0-test4/2.1(windows build), which is what I play on.

If you have some problem installing or using the script packages, or if you would like to contribute improvements to them, contact me in-game.

Installation
============

### For Mudlet 2.0+ users

* Download the script package you want plus all its dependencies from the **packages** directory. (To download them, simply right click -> save as.)
* Start Mudlet and open the profile you want to install them in(ie connect to MM).
* Open the package manager and install the script packages - no particular order is needed. (To open the package manager, either use the text menu - Toolbox->Package Manager, or the icon menu - the brown box "Package Manager")
* After installing, close and reopen your profile(or Mudlet) to make sure all scripts are loaded correctly. When you login, all scripts should report successful initialization(eg, MM_Util has been successfully loaded) 
* As far as I know, Mudlet doesn't offer versioning of packages yet. If you need to update a package, you basically have to uninstall and install it again(this won't delete saved data for scripts, like locations for MM_Travel, but it will remove any modifications to aliases/triggers/scripts you made)
* Scripts that store a database of information save files in your profile's directory. On Windows, the profile directory is in Users->YourUser->.config->mudlet->profiles->YourMMProfile.

**VERY IMPORTANT** Make sure the filename of the package you download is the same as it is here in the repository (For example, if you try downloading the same package twice, you might get a filename such as MM_Util(1).xml). Mudlet uses the filename to determine the name of the package you are installing, and a mismatch will cause some scripts to malfunction.


List of Packages
================
* [MM_Vitals](#mm_vitals) - track hp/sp/st changes
* [MM_Travel] (#mm_travel) - aids blink/teleportation travel by providing coordinates and distance to your target.
* [MM_Util] (#mm_util) - utility package

### MM_Vitals

Tracks the changes of your vitals(hp, sp, st) and shows them in a concise form on your prompt

#### Configuration
MM_Vitals should automatically track hp/sp changes between consecutive prompts, and display them in square brackets next to the prompt. The script specifically doesn't track st changes only, to reduce spam when walking. 

You can configure the colors the script uses to highlight positive or negative changes of hp/sp by opening Scripts -> MM_Vitals -> MM_Vitals Core and changing the values colorLost and colorGained of MM_Vitals.config. For a list of available colors, see http://www.mudlet.org/asciidoc/manual.html#fg
#### [Sample Usage](http://htmlpreview.github.io/?https://github.com/Sacho/mm_scripts/blob/master/samples/MM_Vitals.html)
#### Aliases
None
#### Dependencies
None

### MM_Travel

MM_Travel is designed to aid blink/teleportation travel. It allows you to *target* a specific zone(e.g. Maldra's Keep), and then shows you the distance from it when you use a sextant. This helps to limit excessive blinking on the Material Plane specifically, after the addition of so many villages limiting recall zones.

#### Configuration
MM_Travel starts with an empty database of zones. You can add coordinates by simply walking into a zone and looking at your sextant - this should automatically add the zone to the database. You can find a sample DB in the **db** directory(you'd need to save it to your profile, see the [Installation](#installation) section for where that is).
#### [Sample Usage](http://htmlpreview.github.io/?https://github.com/Sacho/mm_scripts/blob/master/samples/MM_Travel.html)
#### Aliases
* travel set *Zone* - Sets the current zone you are travelling to.
* travel clear - Clears the current zone.
#### Dependencies
* MM_Util

### MM_Util

This is a package of commonly used functions by the other packages. It doesn't offer any gameplay functionality on its own.

#### Configuration
N/A
#### Aliases
None
#### Dependencies
None