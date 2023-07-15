## Volume Control Script

This script allows you to control the volume of your system using keyboard shortcuts. It is implemented using AutoHotkey.

### Functionality

- Pressing `Win + Up Arrow` increases the volume.
- Pressing `Win + Down Arrow` decreases the volume.
- Pressing `Win + Left Arrow` mutes the volume.
- Pressing `Win + Right Arrow` unmutes the volume.

### Setup

1. Make sure you have [AutoHotkey](https://www.autohotkey.com/) installed on your system.
2. Download the [volume_control.ahk](./volume_control.ahk) script.
3. Double-click on the script file to run it.

### Persistence

If you want the script to run automatically upon Windows startup:

1. Create a shortcut of the script file.
2. Press `Win + R` to open the Run dialog.
3. Type `shell:startup` and press Enter to open the Startup folder.
4. Move the shortcut of the script to the Startup folder.

Alternatively to put it simply, “C:\ProgramData\Microsoft\Windows\Start Menu\Programs\StartUp” is the location of the Startup folder for all users on Windows 11 and 10.

### Single Instance

The script is designed to allow only one instance to run at a time using the `#SingleInstance` directive. This prevents multiple instances of the script from running simultaneously.

```ahk
#SingleInstance, Force

#Up::
    Send {Volume_Up}
    return

#Down::
    Send {Volume_Down}
    return

#Left::
    Send {Volume_Mute}
    return

#Right::
    Send {Volume_Mute}
    return

