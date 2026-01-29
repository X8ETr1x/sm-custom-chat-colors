# Changelog

## [3.2.0] 2026-01-29

### Changed

- Updated to new declarations.
- Replaced Simple Chat Processor with newer Chat Processor.
- Replaced GetClientAuthString with GetClientAuthId.

### Removed

- Removed updater plugin.
- Unused code.

## [3.1.0] 2014-08-30
        
- Added support for Steam3 IDs

## [3.0.0] 2013-07-08

- Removed deprecated natives
- Added CCC_OnColor and CCC_OnChatMessage forwards
- Deprecated CCC_OnTagApplied, CCC_OnNameColor, and CCC_OnChatColor forwards
- Improved Updater integration

## [2.4.0] 2013-02-11

- Added CCC_OnConfigReloaded forward

## [2.3.0] 2013-01-27

- Added support for CS:GO

## [2.2.0] 2013-01-16

- Added CCC_OnUserConfigPreLoaded forward so other plugins can block the config file from being loaded

## [2.1.0] 2012-12-08

- Added library registration so that other plugins can verify that Custom Chat Colors is running

## [2.0.0] 2012-11-25

- Improved and revised natives

## [1.8.0] 2012-09-27

- Changed update URL to SVN repository
- Plugin now properly fails to load when Simple Chat Processor is not installed

## [1.7.0] 2012-09-16

- Fixed a bug that caused people to improperly receive colors and tags

## [1.6.0] 2012-09-16

- Renamed forwards to add CCC_ prefix
- Added CCC_OnUserConfigLoaded forward
- Added CCC_SetNameColor, CCC_SetChatColor, CCC_SetTagColor, and CCC_SetTag natives

## [1.5.0] 2012-08-25

- Plugin now warns on load if simple-chatprocessor.smx is not loaded

## [1.4.0] 2012-07-12

- Added ability to disable automatic updating

## [1.3.0] 2012-07-03

- Fixed a problem with the OnNameColor forward

## [1.2.0] 2012-06-14

- Made the natives actually work

## [1.1.0] 2012-06-14

- Added OnTagApplied forward
- Added CCC_GetNameColor, CCC_GetChatColor, CCC_GetTagColor, and CCC_GetTag natives

## [1.0.0] 2012-06-02

- Initial release
