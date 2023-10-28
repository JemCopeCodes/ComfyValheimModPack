# ComfyValheimModPack

This repository contains all of the folders for the mods I maintained the Thunderstore pages for in the Thunderstore Upload Format. The mods I maintained were ones that we used in the Comfy Mod pack, mostly written by redseiko but some of these mods are from Nexus and weren't available on Thunderstore at the time. You can also find the [ComfyModpack](https://github.com/JemWritesCode/ComfyValheimModPack/tree/main/ComfyValheimPack) itself and the older version of my Admin pack in this repo. This repo primarily served as a backup and for ease of use while updating things-- but you can find all of the relevant files and their version history on Thunderstore itself. 

# Comfy Valheim Pack

The [ComfyValheimPack](https://valheim.thunderstore.io/package/ComfyMods/ComfyValheimPack/) is mostly a list of dependencies, but some mods were packed into it directly (such as custom loading screens so I could pick the screens).

Some mod folders are created from mods that allowed upload permission per their [Nexus](https://www.nexusmods.com/) mod page but they are not mine. Please check with the individual creators in those cases.

# Simple Mod Updating
To upload to the [Thunderstore Valheim Upload Page](https://valheim.thunderstore.io/package/create/) you need a zipped folder with `icon.png`, `README.md`, and `manifest.json` as well as whatever files are needed for the mod(usually just a .dll file). More info on these requirements can be found on the [Thunderstore Upload page](https://valheim.thunderstore.io/package/create/) (specifically look in the [Package Format Documentation](https://valheim.thunderstore.io/package/create/docs/))

1. Download this github repository and go to the folder of the mod you wish to update
2. Drag in the new .dll file
3. Increase the version in the manifest file
4. If you need to, update the `manifest.json` file to add any new dependencies. You can get the dependency string that goes into this array from the page of the mod you want as a dependency.
5. Zip up all the needed files in the folder and upload it to [Thunderstore Valheim Upload Page](https://valheim.thunderstore.io/package/create/)

Thunderstore doens't make it easy to delete mods at the time of this writing. If you need to delete for some reason you'll have to go to their discord and request it be done manually. 

# Adding a mod to the Comfy ModPack
Be careful with which mods you add to the Comfy Modpack-- people who have it installed will be forced to have all the mods in the pack or else disable the pack (which would stop them from getting future updates). Generally only add mods that everyone will use.
1. Get all of the files from https://github.com/JemCopeCodes/ComfyValheimModPack/tree/main/ComfyValheimPack
2. Update the `manifest.json` file by going to the dependencies array and adding another element with the dependency string(this will be on the Thunderstore mod page) from the mod you wish to add to the pack.
3. Increase the "version_number" on `manifest.json`
4. Zip up all the files in this folder(including config and plugins) and upload it on the [Thunderstore Valheim Upload Page](https://valheim.thunderstore.io/package/create/)
