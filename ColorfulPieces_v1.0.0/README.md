# ColorfulPieces

  * You can color any building piece that can be built using the Hammer using RGB or HTML color codes.
    * Coloring is very simple at the moment and will color all materials/textures on the object (to be refined later).
    * Those without the mod installed will still see the default vanilla materials/textures.

  1. In-game, press F1 to bring up the ConfigurationManager and navigate to the ColorfulPieces section.
     * Change the target color using the RGB sliders or using an HTML color code.
     * Change the target emission color factor using the slider (this affects how bright the target color will be).
  2. Hover over any building piece ***that you are the owner of*** and a prompt will appear.
     * Hit `LeftShift + R` to change the building piece color to the target color and emission factor.
     * Hit `LeftAlt + R` to clear any existing colors from the building piece.
     * Hit `LeftCtrl + R` to copy the existing color from a piece.
     * This prompt can be hidden by disabling the `showChangeRemoveColorPrompt` setting.
     * Prompt font-size can be configured with the `colorPromptFontSize` setting.



Looking for a chill server? Join us on [Comfy Valheim Discord](https://discord.gg/ameHJz5PFk)
Github: [https://github.com/redseiko/ComfyMods](https://github.com/redseiko/ComfyMods)

Looking for great Valheim servers to play on? Check out our community driven listing site at [https://valheimlist.org](https://valheimlist.org)

## Changelog

### 1.3.0

  * Fixed `PieceEmissionColorFactor` not being copied during copy color action.
  * Renamed `LastColoredBy` to `PieceLastColoredBy` to be more consistent with other colorful mods.
  * Added an option to change the font-size for the text prompt on hover.

### 1.2.1

  * Recompiled against H&H patch.

### 1.2.0

  * Fixed for Hearth & Home update.
  * Added new action to copy the (existing) color of the hovered piece.
    * Defaults to `LeftCtrl + R`.
  * All keyboard shortcuts for actions (including set color and clear color) are now configurable.
  * Increased maximum emission factor from `0.6` to `0.8` to allow for brighter colors.
  * Added a new `LastColoredBy` long ZDO property set to the PlayerId on set or clear.

## 1.1.0

  * Fixed a memory leak causing the game to crash/freeze during a player profile save.
    * This is because we used ConditionalWeakTable to cache piece materials but the Unity docs state that
      UnityEngine.Object does not support WeakReferences.
    * Changed to a Dictionary instead and patch `WearNTear.OnDestroy()` to remove the reference.
  * Added configuration setting to hide the 'change color' and 'remove color' prompt over a ward.

## 1.0.0

  * Initial release.