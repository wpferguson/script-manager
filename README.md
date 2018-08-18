# script-manager
a darktable script management solution

script_manager - cross platform lua scripts management

## Description

**script_manager** is designed to make the darktable lua scripts
accessible to everyone without having to edit files or use 
commands they aren't comfortable with.  

**script_manager** is meant to replace the luarc file in the 
darktable configuration directory.  When darktable starts it looks 
for the luarc file and loads it.

With **script_manager** you can install, update, or reinstall the lua 
scripts.  You can turn individual scripts on or off with the click of 
a button.  Scripts are divided into "categories" based on the lua 
subdirectory they are located in.  For the lua scripts distribution
the categories would be contrib, examples, official, and tools.

## ADDITIONAL SOFTWARE NEEDED FOR THIS SCRIPT
* git - https://git-scm.com/

## INSTALLATION

### Linux and MacOS
* make sure git is installed
* download (or clone the repository of) script_manager
* copy script_manager.lua to $HOME/.config/darktable/luarc

### Windows
* make sure git is installed.  I use https://gitforwindows.org.
* download (or clone the repository of) script_manager
* copy script_manager.lua to C:\Users\<username>\AppData\Local\darktable\luarc


## USAGE
* install script_manager
* start darktable
* go to the configuration tab and specify the location of git, if necessary
* click install to install the scripts from the specified repository (default:
  https://github.com/darktable-org/lua-scripts.git), if they aren't already.
* click update to retrieve the latest version of the scripts from the
  specified repository (default: https://github.com/darktable-org/lua-scripts.git)
* activate the scripts you want 

## USAGE NOTES
* deactivate doesn't take effect until darktable is restarted.  The Lua API doesn't support
  removing loaded scripts or GUI elements.
* Newer scripts retrieved using update won't take effect until darktable is restarted
  since we can't unload running scripts.  A script that isn't active and gets updated
  will run the newest version if activated after the update.

## BUGS, COMMENTS, SUGGESTIONS
* Send to Bill Ferguson, <wpferguson@gmail.com>

