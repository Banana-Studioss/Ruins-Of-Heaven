# Ruins Of Heaven's Modding API

### Ruins Of Heaven Introduced Modding API, Allowing Players To Create And Import Mods.
### Ruins Of Heaven Uses Lua For The Framework. For Mods To Hook Onto Events, They Must Use ```Banana.Mod```

# --------- MOD GUIDE -----------
# If Your Not Looking To Create Mods, Scroll Down To "MOD SETUP"

## Creating A Mods Folder.
### Go To The Dir Where Your Ruins Of Heaven .exe Is, If Your Using Ruins Of Heaven+ DLC You Should See A "Mods" Folder.
### A Mod Folder Must Contain A metadata.txt, Thats How The Mod Is Ran.
### Next, Create A Folder In That Mod Folder, Named "Scripts", Inside It, Create "main.banan", This Is Where You'll Code Your Script.
### You Can Make A "Images", "Sounds", "Music", "Fonts", etc Folder Next To Scripts For Your Mod To Use.

## Actually Scripting The Mod.
### The Entire Script Needs To Be Lua (Not C++ Or C#)
### For Your Mod To Actually Run In The First Place, Put At The Top Of Your Script ```Banana.Mod.RunMod()```, The Game Will Then Load The Mods Contents.

## Hooking Onto An Entity
### Entities Have IDs When They Spawn (Ben Is 1, Mercedes Is 2 For Example). 
### You Can Fetch The IDs Of Entities Using ```Banana.Mod.FetchIDs({name})```
### You Can Edit Properties Of That Entity Using ```Banana.Mod.Property({property},{value},{entityid})```, Some Properties Won't Work (Like Giving An Enemy Ben's Laser Property)
### You Can Also Kill The Entity Using ```Banana.Mod.Kill({entityid})```

## Granting An Item (Rebirth Of Heaven DLC Required!)
### You Can Grant Both Players An Item Using ```Banana.Mod.ItemGrant({ID})```
### And Remove The Item Using ```Banana.Mod.ItemRemove({ID})```

# --------- MOD SETUP ---------

## Setting Up A Mod Is Easy.
### First, Find The Mod You Want (usually at ruinsofheaven.com/modding/ or Itch.io)
### Install The .bananmod File
### Place The .bananmod File In Your Mods Folder
### Ruins Of Heaven Will Unpack It, Read It, And Load It.
### (You Can Upload Your Own Mods To ruinsofheaven.com/modding/)!
