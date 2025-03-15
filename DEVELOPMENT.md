# Development

This file documents various adjustments and tweaks to ensure your workflow is as smooth as possible.

## CSSE

### Resizing Windows

Some windows in the CSSE (Render, Object, Cell, etc) might not save their repositioning and resizing settings
between sessions. To resolve this directly modify the Registry settings under:

```
HKEY_CLASSES_ROOT/VirtualStore/MACHINE/SOFTWARE/WOW6432Node/Bethesda Softworks/TES3 Editor
```

**Alternatively**, simply start CSSE in Admin mode and then resize the windows. Running as an Admin allows the
CSSE to edit the above Registry settings, meaning subsequent launches will keep the adjustments without needing
to be an Admin.

### Launching Morrowind

### Steam Error, Application Load Error 5

If you get this error copy *steam.exe* to your *your steam library/steamapps/common* directory. An alternative
method is to create a symlink.

### Disabling the launcher

For the various CSSE launch settings to work (position, from save) the launcher needs to be disabled. This can
be achieved by adding the following to Steam's launch options for Morrowind (can be reached under *Right Click
->Properties...*):

```
"C:\Games\steamapps\common\Morrowind/Morrowind.exe" %command%
```