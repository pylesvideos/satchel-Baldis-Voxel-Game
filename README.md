A fork of Satchel that includes tabs that can be toggled and are sorted by the tags of tools. It also moves the search bar to above the backpack UI and it disables tool dragging out of the hotbar.

Differences to the original Scatchel:
tabs
moved search bar
cannot drag tools from the hotbar
changed font to cartoony

Configuration: Blocked category tags
----------------------------------

You can prevent certain tags from creating categories (or from being used as a tool's category) by setting the `BlockedCategoryTags` attribute on the `init` ModuleScript. It supports either:

- A comma-separated string, e.g. `"Tool,Admin,Hidden"` — this will block any tag named `Tool`, `Admin`, or `Hidden` (case-insensitive).
- A table of strings, e.g. `{ "Tool", "Admin", "Hidden" }` — also case-insensitive.

Example (ModuleScript attribute):

1. Open the `init` ModuleScript in Roblox Studio.
2. Add an attribute named `BlockedCategoryTags` with value `Tool,Admin,Hidden` (string), or with a table value.

The script will skip blocked tags when determining a tool's category and will not register blocked categories in the category bar.
