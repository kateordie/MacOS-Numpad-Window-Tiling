# MacOS Numpad Window Tiling
These shell scripts address a particular window tiling behaviour in MacOS that drives me nuts: the Globe / Fn key doesn't exist on external keyboards. I've found that remapping the tiling functionality to Ctrl-Opt-Arrow Key works in most applications, but there are a small handful where it won't function. The OOTB keystrokes also don't account for tiling windows into corners. 

There are two shell scripts here - one that restores OOTB window tiling hotkeys, and one that moves to a new set of hotkeys better suited for use with third-party keyboards and on desktop. The functionality present assigns window tiling to the numpad: 

-Window tiling in each of the cardinal directions and each of the four corners is assigned to Ctrl-Opt-1,2,3,4,6,7,8,9

-Centre is assigned to Ctrl-Opt-5

-Fill is assigned to Ctrl-Opt-Plus

-Return to Previous Size is assigned to Ctrl-Opt-Minus

I don't really use the Move and Arrange functions in my desktop workflow, so they're disabled. If you don't like this behaviour, remove the defaults writes for keys 248, 249, 250, 251, and 256.

I like using default tiling controls while using my laptop's built-in keyboard, so I've got a second script to flip back to OOTB settings.

## Installation
In Terminal, chmod each shell script to be executable with: 
```
chmod +x DesktopKeystrokes.sh
chmod +x OrigKeystrokes.sh
```

I find these are most useful with a Shortcut because you can trigger them via an automation or put them in the Control Centre. If you make a Shortcut, add a "Run Shell Script" action. Point at the directory you've put them, e.g.

```
zsh ~/ShellScripts/DesktopKeystrokes.sh
```
In terms of Shortcut automations, I find "When a display is connected / disconnected" super useful to trigger these.


## Usage
In Terminal:
```
./DesktopKeystrokes.sh
./OrigKeystrokes.sh
```

## License
GNU General Public License v3.0
