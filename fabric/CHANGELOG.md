# Changelog

## 1.7.0

### Summary

This update makes PC upgrades and the Remote PC much more configurable on the server side.

### Added

- Added server configuration support to choose which tier is required before the Remote PC can be used
- Added separate options to enable or disable:
  - Remote PC item use in hand
  - Remote PC opening through the keybind
  - Remote PC opening through Trinkets
- Added support for changing the required item for each upgrade
- Added support for changing the required amount for each upgrade
- Added support for changing the displayed names of upgrade tiers

### Improved

- Improved Remote PC progression so it can now be reserved for a specific tier such as Nether Star
- Improved server flexibility by allowing Remote PC unlock difficulty to be adjusted without modifying the mod code
- Improved upgrade cost customization for different server economies
- Improved tier display customization by allowing displayed names to be changed without affecting internal tier identifiers

### Notes

- Internal tier IDs should not be modified in the config
- Recommended config values to customize are:
  - `displayName`
  - `cost.item`
  - `cost.count`
  - `remotePc.requiredTier`
  - `remotePc.enabled`
  - `remotePc.allowItemUse`
  - `remotePc.allowKeybind`
  - `remotePc.allowTrinket`
- By default, the Remote PC is configured to unlock at the Nether Star tier

## 1.6.0

### Summary

This update adds dedicated Alpha and Shiny boxes, while stabilizing the number of free boxes across all upgrade tiers.

### Fixed

- Fixed several wallpaper translations in French and English
- Fixed the missing direct `/cpe reload` command

### Added

- Added dedicated boxes for Alpha Pokémon
- Added dedicated boxes for Shiny Pokémon
- Added prioritized automatic sorting for Alpha and Shiny Pokémon
- Added 16 fixed free boxes for all upgrade tiers
- Added `/cpe reload`

### Improved

- Improved automatic sorting so Alpha Pokémon are now sent to Alpha boxes
- Improved automatic sorting so Shiny Pokémon are now sent to Shiny boxes
- Improved priority handling so Alpha Shiny Pokémon are sorted into Alpha boxes first
- Improved automatic mapping so Alpha, Shiny, and free boxes are now shown more clearly
- Improved `/cpe sort preview` and `/cpe sort now` so they now include Alpha and Shiny boxes
- Improved the config reload message so it now includes the `[CPE]` prefix for clearer mod identification
- Improved free box stability so the number of free boxes now stays consistent across all upgrade tiers

### Notes

- The Nether Star tier now contains 276 boxes in total:
  - 252 type boxes
  - 4 Alpha boxes
  - 4 Shiny boxes
  - 16 free boxes
- Alpha and Shiny boxes are intentionally not split by type in order to keep the PC readable and stable

## 1.5.0

### Summary

This update improves PC box stability and completes missing translation coverage.

### Fixed

- Fixed the PC sometimes reopening on Box 2 instead of the expected box
- Fixed unstable box return behavior after closing the box rename screen
- Fixed unstable box return behavior after closing the wallpaper picker
- Fixed unstable box return behavior after closing the Box Navigator
- Fixed Box Navigator returning to the wrong box after closing
- Fixed box return behavior when using `Go to box` from the Box Navigator
- Fixed the Remote PC keybind displaying a raw translation key
- Fixed missing keybind category translation
- Fixed missing Box Navigator help tooltip translation
- Fixed missing Remote PC requirement message translation

### Improved

- Improved first PC open behavior so it now opens on Box 1 after joining
- Improved PC reopen behavior so it now returns to the last used box during the same session
- Improved box return behavior after rename, wallpaper selection, or box navigation so it now preserves the intended box
- Improved PC behavior without requiring MCT to be installed
- Improved return flow by reducing the visible delay before restoring the correct box
- Improved French and English translation coverage
- Improved polish in the controls menu and in-game messages

## 1.4.0

### Summary

This update adds support for custom PC box wallpapers through resource packs.

### Added

- Added support for custom wallpapers loaded from resource packs
- Added automatic detection of `.png` files placed in `assets/cobblepcenhanced/textures/gui/pc/wallpapers/custom/`
- Added custom resource pack wallpapers to the wallpaper picker
- Added save support for custom wallpapers selected per box

### Improved

- Improved wallpaper customization so custom wallpapers can now be added without modifying or rebuilding the mod
- Improved separation between custom wallpapers and the public mod jar
- Improved compatibility of custom wallpapers with renamed boxes and free boxes
- Improved wallpaper customization workflow for private packs, server packs, and personal use

### Notes

- Recommended wallpaper size: `208x189`
- Badly cropped or overly detailed images may not display cleanly behind the PC grid

## 1.3.0

### Summary

This update improves the PC interface with new wallpapers for free boxes, a box navigator, and a built-in box renaming system directly integrated into the UI.

### Fixed

- Fixed raw translation text that could appear in the wallpaper picker
- Fixed raw translation text in the renaming UI
- Fixed the Rename button in the box navigator showing a raw translation key
- Fixed box name reset behavior so it now restores the logical mapped name instead of reverting to the vanilla `Box X` name
- Fixed several compilation issues related to the wallpaper picker and box navigator during integration

### Added

- Added new wallpapers for free boxes
- Added a box navigation button in the PC interface
- Added a small box search UI
- Added box search by number, name, type, or custom name
- Added previous / next buttons to navigate through search results
- Added a button to jump directly to the selected box
- Added box renaming from the box navigator
- Added a dedicated button to rename the currently opened box directly
- Added a reset button for box names
- Added a nametag-style icon for the rename button
- Added a help tooltip for the box navigator

### Improved

- Improved custom box name saving
- Improved custom box name persistence after closing and reopening the PC
- Improved custom box name persistence after disconnecting and reconnecting
- Improved box name reset behavior so it now restores the logical mapped name such as `Steel 2` or `Free 4` instead of reverting to the vanilla `Box X` name
- Improved the box navigator so it works without affecting the existing Pokémon search
- Improved compatibility with the existing sort buttons
- Improved the visual polish of the renaming UI
- Improved FR / EN translations for the box navigator and renaming UI

### Notes

- This update keeps the existing sorting logic intact
- Renamed boxes remain compatible with wallpapers
- Wallpapers, box navigation, and renaming were validated after closing and reopening the PC and after disconnecting and reconnecting

## 1.2.0

### Summary

This update improves Remote PC usability by adding Trinkets integration and a configurable keybind to open the PC without having to hold the item in hand.

### Added

- Added a dedicated Trinkets slot for the Remote PC
- Added a discreet icon for the remote slot
- Added a configurable keybind to open the PC while the Remote PC is equipped
- Added a clean feedback message when the player tries to use the keybind without having the Remote PC equipped

### Improved

- Improved Remote PC usability by allowing it to be used directly from its dedicated Trinkets slot
- Improved keybind safety by leaving the PC open key unbound by default to avoid conflicts with existing controls
- Improved consistency by keeping right-click behavior unchanged when using the Remote PC normally
- Improved visual polish by removing the visual cooldown after using the Remote PC

### Notes

- The wallpapers added in 1.1.0 were not modified
- The dedicated Trinkets slot is separate from other mod slots such as Academy

## 1.1.0

### Summary

This update adds a complete wallpaper system for Cobblemon PC boxes, with custom type-based textures, persistent saving, and clean integration into the PC interface.

### Added

- Added custom wallpapers for Cobblemon PC boxes
- Added textures for all main Pokémon types:
  - Fire
  - Water
  - Grass
  - Electric
  - Ground
  - Poison
  - Steel
  - Ghost
  - Fairy
  - Dark
  - Psychic
  - Ice
  - Dragon
  - Bug
  - Rock
  - Normal
  - Fighting
  - Flying
- Added wallpaper previews in the selection UI
- Added per-box wallpaper saving

### Improved

- Improved wallpaper integration in the Cobblemon PC interface
- Improved rendering of the frame around the PC box grid
- Improved wallpaper sizing to avoid UI overflow
- Improved slot border readability to keep the grid clear
- Improved wallpaper persistence when switching boxes
- Improved wallpaper persistence after closing and reopening the PC
- Improved wallpaper persistence after disconnecting and reconnecting
- Improved compatibility with the PC sorting buttons
- Improved compatibility with CobblePCEnhanced global sorting

### Notes

- This update focuses only on PC wallpapers
- The next planned update is focused on Trinkets integration for the remote item, with a quick-open keybind

## 1.0.0

### Summary

Initial release of CobblePCEnhanced, adding PC upgrades, automatic type-based organization, and core storage quality-of-life features for Cobblemon.

### Added

- Added the CobblePCEnhanced PC upgrade system
- Added multiple PC upgrade tiers
- Added increased Pokémon storage capacity through upgrades
- Added automatic Pokémon sorting by primary type
- Added type-based box mapping
- Added automatic box naming based on Pokémon type and box index
- Added support for keeping type boxes organized across upgraded PC tiers
- Added per-player PC organization support
- Added manual sorting controls
- Added search and sorting quality-of-life tools
- Added safer handling for Pokémon movement between boxes
- Added core configuration support
- Added commands for managing and debugging PC behavior
- Added English and French translation support

### Improved

- Improved the Cobblemon PC workflow for large Pokémon collections
- Improved readability of organized boxes
- Improved long-term storage management for players who collect many Pokémon
- Kept the UI close to the original Cobblemon PC style

### Notes

- This is the first stable release of CobblePCEnhanced
- The mod is designed to be installed on both client and server
- Cobblemon is required
