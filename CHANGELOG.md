# 2.1.3 Whips and Chains

## What's New

* Search configuration pinning: Can now right click on the search config button in the workshop (wrench icon) to "pin" it and keep it expanded while performing searches. Right click again to un-pin and return to normal auto-collapsing operation.

## Fixes

* FilePicker Workshop launch button injection strengthened: Now checks for explicit upload permissions instead of presence of upload button. 
  * Workshop button has been **moved** from the bottom right of the dialog (near upload button) to the **top navigation tab header.**
  * The FilePicker app to which the active Workshop app is bound will now keep its workshop button toggled or highlighted to indicate the active picker for the Workshop.
  * Opening the workshop from another instance of a FilePicker will now rebind the current workshop (if it exists) instead of fully re-constructing.
  * When the current directory of the bound FilePicker is not a valid upload destination for the current user, the Workshop's import path display will reflect this. Additionally, when the Workshop is in *any* state that does not allow uploading, the Workshop import buttons will be disabled.

* Preset Picker now checks for permission to stock border folder before rendering and gracefully shows a warning notification to the user indicating the browse error.

# 2.1.2 - Single Town

## Fixes
* Re-opening the workshop from the FilePicker paintbrush button will now detect if an active workshop application is rendered already and open/maximize it instead of re-rendering and breaking display styles.
* Strengthened FilePicker target path parsing by using `decodeURI` instead of performing an element query. This allows continued workshop operation even if the bound file picker is closed.
* When importing favorited images/tokens, if the bound FilePicker is closed, it will be opened and re-rendered upon import success.

# 2.1.0 (2.1.1) - Artoe's Laminator

## What's New
* New search categories: `Scenes` and `Token Borders`
* Artoe's Laminator: Companion application to Melvin's Workshop for quickly creating tokens from favorited images or search results.
* `Workshop` and `Laminator` classes exposed via the module's API.
  * `game.modules.get('mels-masterworks').Workshop` and  `game.modules.get('mels-masterworks').Laminator`, respectively.
* Workshop now launches in "offline" mode, allowing access to Artoe's Laminator when the remote server is down or for laminating local assets.
  * Configuration dropdown expanded by default until the first search is performed.

## Fixes
* Remove empty `systems` field in manifest.
* Including `node_modules` in build process.
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
