# script-manager
Darktable script management solution

  script_manager - a drop in luarc file that provides script management

  script_manager creates two modules, Script Install/Update and Script
  Controller.  Script Install/Update installs the scripts, from the
  specified repository, if they don't exist.  Once the scripts are 
  installed the module provides a way to update the scripts with one
  click.  After the scripts are installed, Script Controller starts.  A
  button for each script is displayed.  Hovering over the button displays 
  the documentation from the script. Clicking the button loads the script
  and runs it.  A preference is updated to record that the script is active.
  Once a script is active, the button changes to Deactivate to turn off the
  script.

  ADDITIONAL SOFTWARE NEEDED FOR THIS SCRIPT
  * git - https://git-scm.com/

  USAGE
  * replace the existing luarc file with this one.  
  * start darktable
  * click install to install the scripts from the specified repository (default:
    https://github.com/darktable-org/lua-scripts.git), if they aren't already.
  * click update to retrieve the latest version of the scripts from the
    specified repository (default: https://github.com/darktable-org/lua-scripts.git)
  * activate the scripts you want 

  CAVEATS
  * deactivate doesn't take effect until darktable is restarted.  There currently isn't
    a way to unload a script from the UI (that I'm aware of).
  * Newer scripts retrieved using update won't take effect until darktable is restarted
    since we can't unload running scripts.  A script that isn't active and gets updated
    will run the newest version if activated after the update.
  * changing the repository, then clicking update will cause the current lua directory
    ($HOME/lua-scripts) to be removed and a new one created by cloning the specified
    repository.

    BUGS, COMMENTS, SUGGESTIONS
    * Send to Bill Ferguson, wpferguson@gmail.com

