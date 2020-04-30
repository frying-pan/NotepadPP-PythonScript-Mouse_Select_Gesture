# NotepadPP-PythonScript-Mouse-Gesture

Add keyboard + mouse gestures to Notepad++ when the script is run from Notepad++ (with PythonScript plugin installed)

via a window procedure hook on Notepad++ Scintilla child windows


Tested with Notepad++ 7.8.2 64 bits, with PythonScript plugin 1.5.2,

on Windows 8.1 64 bits (NOT tested with Notepad++ 32 Bits but could be compatible)


Features :
  * SHIFT + double-left-click        : select from clicked point the whole variable name : alphanumeric with _ and . (dot)
  * CTRL + SHIFT + double-left-click : select from clicked point the whole bracket content : () [] {}, from left in case of mismatch
  * ALT + SHIFT + double-left-click  : select from clicked point the whole quote content : "" '', from left in case of mismatch
  * ALT + right-click                : select from clicked point until space/space-like characters are met : space/tab/cr/lf/formfeed/vtab etc...
  * right-click                      : prevent right-click from moving the caret and losing current text selection


# Install :

This script can be run at Notepad++ startup (folders below are those of a local installation) : 

* copy the main Perso_ScintWndProc_Hook .py script file (and starting from v3 the needed libraries files) in :

C:\Users\[username]\AppData\Roaming\Notepad++\plugins\config\PythonScript\scripts

* add "import [Perso_ScintWndProc_Hook (py) script file name without extension]"

to the startup.py file located, for me, under the Notepad++ install folder :

C:\Program Files\Notepad++\plugins\PythonScript\scripts

(I think I had to take ownership of startup.py before being able to write into it)


# Versions :

Perso_ScintWndProc_Hook_v1_0.py, (updated to Perso_ScintWndProc_Hook_v1_1.py for a small bug)
is somewhat more tested.

Perso_ScintWndProc_Hook_v2_0.py, (updated to Perso_ScintWndProc_Hook_v2_1.py for the same small bug as v1_0)
changes :
* code reorganized/cleaned
* more object oriented
