## Satchel (Baldi's Voxel Game fork)

Satchel is a modern, customizable replacement for Roblox's default backpack. This fork adds tabbed categories (driven by tool tags), moves the search bar above the inventory, restricts hotbar dragging, and includes an option to block specific tags from producing categories.

## Features
- Tabbed categories derived from tool tags
- Search bar placed at the top of the inventory UI
- Hotbar tools cannot be dragged out of the hotbar (only inventory → hotbar moves allowed)
- Option to block tags from creating categories (`BlockedCategoryTags`)

## Configuration
### Blocked category tags

You can prevent certain tags from creating categories (or from being used as a tool's category) by setting the `BlockedCategoryTags` attribute on the `init` ModuleScript (`src/init.luau`). The attribute supports either:

- A comma-separated string (case-insensitive), e.g. `Tool,Admin,Hidden`
- A Lua table of strings, e.g. `{ "Tool", "Admin", "Hidden" }`

Behavior:
- When determining a tool's category, the script will skip any tags listed in `BlockedCategoryTags`.
- Blocked categories will not be registered in the category bar.

Example (Roblox Studio):

1. Open the `init` ModuleScript in Roblox Studio (the script in `src/init.luau`).
2. Add an attribute named `BlockedCategoryTags` and set its value to either:
	- A string: `Tool,Admin,Hidden`
	- A table: `{ "Tool", "Admin", "Hidden" }`
