# sm-custom-chat-colors

A fork of [Dr. McKay's plugin](https://forums.alliedmods.net/showthread.php?t=186695).

Description:
Give particular Steam IDs and admin flags custom chat colors and name tags. Supports any color you can imagine, or team color, green, and olive. This is a rewrite of Simple Chat Colors (Redux). Requires Simple Chat Processor (Redux). Complete documentation is in the config file.

Only works in Source 2013 games, which include:

    Team Fortress 2
    Counter-Strike: Source
    Half-Life 2: Deathmatch
    Day of Defeat: Source


This also works on CS:GO, but only "T", "G", and "O" codes can be used.

Update: I'm getting reports that colors don't work on CS:GO when alive. This is a shame, but this plugin doesn't officially support CS:GO. Don't expect it to be fixed.


This plugin will never support any CS:GO colors beyond those mentioned above, so stop asking.

Commands:
sm_reloadccc - reloads the config file

Cvars:
custom_chat_colors_version - plugin version
custom_chat_colors_auto_update (default 1) - enables automatic updating (has no effect if Updater is not installed)

Requirements:
Requires the Simple Chat Processor (Redux) plugin.

Developers:
This plugin provides several forwards and natives. See the include file for documentation.

Installation:
Install Simple Chat Processor (Redux), extract chatcolors.zip, upload its contents to your /addons/sourcemod directory, and reboot your server or type "sm plugins load custom-chatcolors" into your console or rcon.

Auto Update:
Install Updater. The plugin will be auto-updated according to your Updater settings. It'll work without Updater.

Changelog:

    v3.1.0 (8/30/14)
        Added support for Steam3 IDs
    v3.0.0 (7/8/13)
        Removed deprecated natives
        Added CCC_OnColor and CCC_OnChatMessage forwards
        Deprecated CCC_OnTagApplied, CCC_OnNameColor, and CCC_OnChatColor forwards
        Improved Updater integration
    v2.4.0 (2/11/13)
        Added CCC_OnConfigReloaded forward
    v2.3.0 (1/27/13)
        Added support for CS:GO
    v2.2.0 (1/16/13)
        Added CCC_OnUserConfigPreLoaded forward so other plugins can block the config file from being loaded
    v2.1.0 (12/8/12)
        Added library registration so that other plugins can verify that Custom Chat Colors is running
    v2.0.0 (11/25/12)
        Improved and revised natives
    v1.8.0 (9/27/12)
        Changed update URL to SVN repository
        Plugin now properly fails to load when Simple Chat Processor is not installed
    v1.7.0 (9/16/12)
        Fixed a bug that caused people to improperly receive colors and tags
    v1.6.0 (9/16/12)
        Renamed forwards to add CCC_ prefix
        Added CCC_OnUserConfigLoaded forward
        Added CCC_SetNameColor, CCC_SetChatColor, CCC_SetTagColor, and CCC_SetTag natives
    v1.5.0 (8/25/12)
        Plugin now warns on load if simple-chatprocessor.smx is not loaded
    v1.4.0 (7/12/12)
        Added ability to disable automatic updating
    v1.3.0 (7/3/12)
        Fixed a problem with the OnNameColor forward
    v1.2.0 (6/14/12)
        Made the natives actually work
    v1.1.0 (6/14/12)
        Added OnTagApplied forward
        Added CCC_GetNameColor, CCC_GetChatColor, CCC_GetTagColor, and CCC_GetTag natives
    v1.0.0 (6/2/12)
        Initial release
