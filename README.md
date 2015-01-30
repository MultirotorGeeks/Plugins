# REPOSITORY NAME

Plugins

# AUTHOR

Paul Rancuret

# DESCRIPTION

This repository contains packaged plugins for eclipse, developed to make life easier for the Multirotor Geeks.  Right now, it only contains one plugin, called the 'Uncrustify' Plugin.  Instructions for installing and using that plugin are provided below.

# UNCRUSTIFY PLUGIN

This plugin allows the user to quickly and easily invoke the 'Uncristify' program from within eclipse.  This program is used to automatically adjust code formatting (white space, variable alignment, etc.) so that it has a clean, consistent look and feel.

To install the Uncrustify Plugin, follow these steps:
* [Download and Install](http://sourceforge.net/projects/uncrustify/files/uncrustify/) the uncrustify program on your computer.
* Clone the [Plugins](https://github.com/MultirotorGeeks/Plugins) repository from git, placing it in a known location on your computer.
* In Eclipse, click Help->Install New Software...
* Next to 'Work With:' enter file:/<path_to_local_Plugins_Repo> where <path_to_local_Plugins_Repo> is the path to the repository you just cloned.
* Select the 'Uncrustify Plugin' checkbox underneath Eclipse Plugins.  (Note: if it doesn't appear, you may already have it installed.  Click on the 'What is already installed?' link to check)
* Click 'Next >' and then follow prompts to install the plugin.
* Configure the uncrustify plugin using the following steps:
 * In Eclipse, click Window->Preferences and then select the 'Uncrustify' menu option on the left.
 * Next to 'Uncrustify path,' browse to the uncrustify.exe program which you just installed.
 * Keeping the 'Modify files in-place' option checked will prevent the program from creating backup copies of each file each time it is modified to clean up code formatting.  Since git version control is used for our files, this should be relatively safe, and will prevent adding a bunch of unnecessary files to version control.
 * In the extension list, provide a comma separated list of file extensions you wish to use the plugin for.  At this point, I am only using it for c,cpp,h files.  However, it can be used for other files as well, depending on the configuration file settings.
 * Next to 'Configuration File,' browse to a configuration file of your choice.  It will have a .cfg extension.  Here are several options for where to obtain a configuration file:
  * The [Plugins](https://github.com/MultirotorGeeks/Plugins) repository contains a configuration file called custom.cfg.  This is the configuration used when cleaning up the source files in the [Arduino](https://github.com/MultirotorGeeks/Arduino) repository.
  * The uncrustify program installation includes some sample configuration files, in the same directory as the executable.
  * You can create your own, or modify an existing one.  The files are standard ascii, so they can be modified by any text editor.  There are online tools such as [UniversalIndentGUI](http://universalindent.sourceforge.net/) which provide a graphical way of creating this file as well.
  
Once the plugin is installed, it can be used to clean code formatting of entire files, or of selections within files.  To clean up one or more files in eclipse, select the file(s) from within the 'Project Explorer,' then right click and select 'Uncrustify Selection.'  To clean up text within a file, simply highlight the text, right click it, and select 'Uncrustify Selection.'