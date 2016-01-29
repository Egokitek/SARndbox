# yksandbox

This branch of SARndbox is for localized settings and of my sandbox setup.

## Folders

___ | ___
~/code/sandbox  | source code editing and staging area, a git repo
~/src           | downloaded archives, and possibly their unpacked contents. No
editing or changes here.
~/sandbox | run-from here, the installed sandbox application and all dependencies. Target
root for `make install`

## Workflow

1. Edit and adjust *code* as needed or desired
2. Update *run-from* folder tree, e.g. `make install`
3. Test run sandbox application
    a. tweak and adjust
    b. merge changes back to code
    c. commit and push back to github

## Install
_Only differences from upstream README noted._

Set Environment

    export INSTALLDIR=$HOME/sandbox 
    export VRUI_MAKEDIR=$HOME/sandbox/share/Vrui-3.1/make

and then for each of Vrui, Kinect and SARndbox run:

    cd ~/src/$program
    make VRUI_MAKEDIR=$VRUI_MAKEDIR
    make install INSTALLDIR=$INSTALLDIR VRUI_MAKEDIR=$VRUI_MAKEDIR

See `yksandbox-install.sh`


## Extras
_Optional tools used on this machine. Useful for administration and
customizing but not essential._

git-cola - light weight graphical interface for git (a bit buggy)
meld - graphical file and folder diff, compare, merge
cream - version of gvim more familiar for Windows users 

