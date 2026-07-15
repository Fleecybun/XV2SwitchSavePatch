DRAGON BALL XENOVERSE 2 — NINTENDO SWITCH OFFLINE SAVE PATCHER GUI
=====================================================================

BACK UP YOUR ORIGINAL savefile1.dat BEFORE USING THIS TOOL.
THE PATCHER WRITES A SEPARATE OUTPUT FILE AND REFUSES TO OVERWRITE THE INPUT.

QUICK START
-----------
1. Install Python 3 for Windows. During installation, enable "Add Python to PATH".
2. Double-click "Install Cryptography.bat" once.
   Manual command: py -3 -m pip install cryptography
3. Drag savefile1.dat onto "Launch XV2 Switch Patcher.bat".
4. Choose the patches in the GUI nd press "Patch Save".
5. Restore/import the newly written *_offline_patched.dat file using your save tool. 
    Make sure to rename to savefile1.dat and zip with the other files in your save data folder.

You can also double-click the launcher without dragging a file, then use Browse.

PATCH OPTIONS
-------------
ALL REGULAR ARTWORK (IDS 1-900)
- Enables the confirmed regular Artwork ownership bits for IDs 1 through 900.
- 900 is the tested safe boundary for this Switch save layout.
- gonna update this but it looks like artworks above 900 are in a different memory location.

ALL CLOTHING
- Adds the latest Tops, Bottoms, Gloves, and Shoes ID lists.
- Includes final-update clothing IDs 529-542 in all four clothing categories.
- Checks the primary clothing "location-lookup" blocks.
- The newer location-lookup extension for IDs 529-542 is not mapped, so those
  items can appear in inventory while remaining unchecked in Location Lookup.
- Location-lookup might show some missing print tees, but they will be in the inventory.

ALL ACCESSORIES
- Adds the last known-working accessory ID list.
- Checks the accessory Location Lookup flags.

ALL SUPER SOULS
- Adds the latest Super Soul ID list through the known sparse IDs.
- Checks the primary Super Soul Location Lookup flags.
- A newly advertised Festival reward may still be unavailable because its real
  inventory item ID is not yet known.

ALL SKILLS
- Enables all existing Super Attack, Ultimate Attack, Evasive, and Awoken records
  in the current save.
- Does not unlock debug skills, aka Unknown Skills, as these crash the game immediately.

99 ZEN-OH BUTTONS / 99 SUPER MIX CAPSULE Z
- Changes only the confirmed count byte and preserves the rest of each item record.

LOBBY ITEMS
-----------
ADD LOBBY ITEM AT OWN RISK, WILL WIPE OUT TP MEDALS

Adding all of the lobby items will make you go broke. you will get every aura, vehicle, mascot, 
including The Power to Overcome, SSJ4 DAIMA, Ultra Supervillain, etc. Whether adding one 
or all lobby items, the TP medals count drops to -2. Cannot add TP medals manually.
Will update if there is a fix.

The GUI requires a second confirmation before applying this option.

DEPENDENCY ERRORS
-----------------
If the launcher says Python is missing:
- Install Python 3 for Windows, reopen the folder, and try again.

If the launcher says cryptography is missing:
- Double-click "Install Cryptography.bat", or run:
  py -3 -m pip install cryptography

If Tkinter is missing, install a normal full Python build rather than a minimal
or embedded distribution.

SAFETY / COMPATIBILITY
----------------------
- Intended for modern Xenoverse 2 Nintendo Switch savefile1.dat files.
- Dynamically reads the encrypted body size; it does not use the old fixed size.
- Recalculates the known save checksums and validates the output after writing.
- Keep multiple backups. Test offline first.
