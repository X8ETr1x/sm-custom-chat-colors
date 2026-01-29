# Custom Chat Colors

A fork of [Dr. McKay's plugin](https://forums.alliedmods.net/showthread.php?t=186695).

Give particular Steam IDs and admin flags custom chat colors and name tags. Supports any color you can imagine, or team color, green, and olive. This is a rewrite of Simple Chat Colors (Redux). 

## Compatibility

- Team Fortress 2: all colors.
- Counter-Strike: Source: all colors.
- Half-Life 2: Deathmatch: all colors.
- Day of Defeat: Source: all colors.

## Installation

- Add the compiled plugin `custom-chatcolors.smx` to `tf/addons/sourcemod/plugins/`.
- Add the addon configuration file `custom-chatcolors.cfg` to `/tf/addons/sourcemod/configs/`.
- Reload all plugins or restart the server.

### Dependencies

- [Chat Processor](https://github.com/X8ETr1x/sm-chat-processor)

## Configuration

The primary configuration file is `tf/addons/sourcemod/configs/custom-chatcolors.cfg`.

- If you don't enter a steamid then the group name does not matter, it's just for your reference.
- For colors, either a hex notation of a color (#RRGGBB or #RRGGBBAA) or one of the supported shortcuts (O - Olive, G - Green, T - Team) is required.

### Order of Operations

The order in which you place items in the config file matters.  Here is what determines what color they get:

1. **SteamID:** If there is a steamid present, it will always override everything.  If you put a steamid in twice then the first entry (top to bottom) will be used. (I think, just don't do it!).
2. **Groups:** The plugin will search (top to bottom) for a postitive match for the flag string.  The player' flags will be compared with the group flag character (NOTE: only one flag per group! "a" is okay, "ab" is NOT), and if the player has the flag, it will stop there. For example. Admins with the "ad" flags and donators with the "a" flag.  If you place the "a" flag group above the "d" group then the admin will get the "a" colors. Order matters.

```
//		"admin_colors"								<--	Leave this alone
//		{											<--	Add all groups/steamids after first bracket (Leave this alone)																			
//			"STEAM_0:1:1234567"						<--	Here is a steamid example with a tag (don't duplicate steamids)
//			{
//				"namecolor"		"#RRGGBB"			<--	This is the color for the name (#RRGGBB in hex notation or #RRGGBBAA with alpha)
//				"textcolor"		"#RRGGBBAA"			<--	This is the color of the text
//			}
//			"groupname"								<--	This can either be a steamid for a specific player, or a group name
//			{										<--	Open the group
//				"flag"				"z"				<--	This is the flag(s) assoicated with the group.  This field doesn't matter if the group name is a steamid
//				"tag"				"[admin]"		<--	This is the text for the tag
//				"tagcolor"		"O"					<--	This is the color for the tag
//				"namecolor"		"G"					<--	This is the color for the name
//				"textcolor"		"T"					<--	This is the color of the text
//			}										<--	Close the group
//		}											<--	Add all groups/steamids before last bracket (Leave this alone)
//
"admin_colors"
{
	"STEAM_0:1:16"
	{
		"tag"				"[BAILOPAN]"
		"tagcolor"			"O"
	}
	"VIP"
	{
		"flag"				"a"
		"tag"				"[VIP]"
		"tagcolor"			"#9EC34FAA"
		"namecolor"			"#00CCFF"
		"textcolor"			"#000000AA"
	}
}
```

## Commands

* `sm_reloadccc`:
  * **Description:** Reloads the configuration.
  * **Required Admin Flags**: config.
