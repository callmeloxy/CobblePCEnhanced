# Changelog

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
