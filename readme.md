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

1. Vrui

    cd ~/src/Vrui-3.1-004
    make INSTALLDIR=$HOME/sandbox
    make install INSTALLDIR=$HOME/sandbox

2. Kinect

    cd ~/src/Kinect-2.8-002
    make VRUI_MAKEDIR=$HOME/sandbox/share/Vrui-3.1/make
    make install INSTALLDIR=$HOME/sandbox

3. SARndbox

    cd ~/code/SARndbox
    make VRUI_MAKEDIR=$HOME/sandbox/share/Vrui-3.1/make
    make install INSTALLDIR=$HOME/sandbox




## Extras
_Optional tools used on this machine. Useful for administration and
customizing but not essential._

git-cola - light weight graphical interface for git (a bit buggy)
meld - graphical file and folder diff, compare, merge
cream - version of gvim more familiar for Windows users 

