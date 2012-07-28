Introduction
============

This repository hosts all my Mudlet script packages for the mud Materia Magica. For information how to install Mudlet packages, [see the Installation Instructions](#Installation). Each package has a complete description, list of dependencies(which other packages are needed), and API reference. Packages are generally tested on Mudlet 2.0-test4(windows build). Individual package notes 

If you have some problem installing or using the packages, or if you would like to contribute improvements to them, contact me in-game.

List of packages
================
[MM_Vitals](#MM_Vitals) - track hp/sp/st changes
[MM_Util] (#MM_Util) - utility package


MM_Vitals
---------

Tracks the changes of your vitals(hp, sp, st) and shows them in a concise form on your prompt

### Configuration and Usage
MM_Vitals should automatically track hp/sp changes between consecutive prompts, and display them in square brackets next to the prompt. The script specifically doesn't track st changes only, to reduce spam when walking. 

You can configure the colors the script uses to highlight positive or negative changes of hp/sp by opening Scripts -> MM_Vitals -> MM_Vitals Core and changing the values colorLost and colorGained of MM_Vitals.config. For a list of available colors, see [http://www.mudlet.org/asciidoc/manual.html#fg]
### Dependencies
None
### API Reference
MM_Vitals:color(value) - Returns the color to display the value with depending on configuration
MM_Vitals:prompt(hp,sp,st) - Given the new values of hp, sp and st, displays the difference compared to the last call.
### Tested on
2.0-test4
MM_Util
-------

This is a package of commonly used functions by the other packages. It doesn't offer any specific functionality on its own.

### Configuration and Usage
N/A
### Dependencies
None
### API Reference
TBD
### Tested on
2.0-test4

Installation
============

### For Mudlet 2.0 users

First, and download the package you want plus all its dependencies from the packages directory(To download them, simply right click -> save as). Open the Mudlet profile you want to install the packages in, and open the package manager(Either through the text menu - Toolbox -> Package Manager, or through the icon menu - the brown box "Package Manager"). Then simply install all the packages (no particular order needed). In order for the packages to start working, you may need to close and reopen your profile.

If you have an old version of a package and want to upgrade, uninstall the package, download the new version and simply install it again.

*** VERY IMPORTANT *** Make sure the package you download is named the same way as it is in the repository (And not, say, MM_Whatever (1).xml.xml). Since mudlet uses filenames to determine the name for the package to be installed, the name must match the one in the repository, or some of the scripts might not work as expected.