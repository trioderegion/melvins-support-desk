# 2.1.0 - Artoe's Laminator

## What's New
* New search categories: `Scenes` and `Token Borders`
* Artoe's Laminator: Companion application to Melvin's Workshop for quickly creating tokens from favorited images or search results.
* `Workshop` and `Laminator` classes exposed via the module's API.
  * `game.modules.get('mels-masterworks').Workshop` and  `game.modules.get('mels-masterworks').Laminator`, respectively.
* Workshop now launches in "offline" mode, allowing access to Artoe's Laminator when the remote server is down or for laminating local assets.
  * Configuration dropdown expanded by default until the first search is performed.

## Fixes
* Workshop now remembers last grid/result size until browser reload.

# 2.0.0 - Binder Full of Creatures

## What's New
* Updated protocol to `0.0.1`
* Result grid and favorited images right-click improvements
  * Unselected image  = preview full res with option to un/favorite.
  * Selected image = removes from saved list.
* UI for categories and tags
  * Collapsable search config menu.
  * Category tags reflect chosen category.
  * `Portraits` and `Creatures` currently available, with `Portraits` having two optional tags to further refine search: `Sci-Fi` and `Fantasy`.
* Loading animation while importing favorited images
* Help button added to Workshop app header, directing to Melvin's Support Desk

## Fixes
* Ensures rendered URI list is at least 49 elements
* Better image sizing for non-square thumbnails
* Parsing FilePicker path field directly as foundry does to avoid `%20` characters
  * Fixes uploading to a folder containing spaces or other special characters.
* Using form-group/stacked styling for sidebar
  * Should help with styling compatibility across systems/UI Mods.
* Updated image licensing text

# 1.2.0 - Open Season

## What's New
* Officially supporting FoundryVTT v9
* Increased responsiveness and sizing considerations of main Workshop app. Minimum tested device height = 768px
