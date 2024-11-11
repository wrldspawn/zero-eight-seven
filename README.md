# zero-eight-seven

A collection of resources for [Momentum Mod 0.8.7](https://github.com/momentum-mod/game/releases/tag/0.8.7-public-eval).
Currently this only focuses on Surf and specifically the map pool used by [KSF](http://ksfclan.com/).

## Zones

Put the `zones` folder from this repo into your `momentum` folder.

## Stripper

[Stripper:Source](https://www.bailopan.net/stripper/) is a plugin that allows modifying maps without having to touch the map file itself.
Momentum Mod does not have any sort of native support for Stripper because "bringing your own map" was never a goal.

A lot of older maps were designed for combat surf only, as skill surf/timer surf did not exist at that time.
Most of these maps have timers and map endings that prevent the map from being played for extended periods of time or being replayed after finishing without reloading the map.

### Setup

1. Install [Metamod:Source](https://www.metamodsource.net/downloads.php?branch=stable) and [SourceMod](https://www.sourcemod.net/downloads.php?branch=stable) into your `momentum` folder

**The normal version of Stripper:Source will not work with Momentum Mod!** It will throw a popup error on map load and more than likely fail.

2. Install [sm-plugin-stripper](https://github.com/srcdslab/sm-plugin-stripper/releases)

This is a rewrite of Stripper:Source as a SourceMod plugin, which is the only reason that SourceMod needs to be installed.

(The provided .tar.gz has a `common` folder inside it that needs to be navigated into revealing an `addons` folder you can put into your `momentum` folder)

3. Put the `stripper` folder from this repo into `momentum/addons/sourcemod/configs/`

4. (Optional) Create a `stripper` folder in `momentum/addons/sourcemod/logs`

This is only needed if you choose to write your own Stripper configs. Running `stripper_dump` will fail without this folder already being created.

### Pitfalls

Configs from other sources will probably not work without modification with the plugin version of Stripper. See [this issue](https://github.com/tilgep/stripper/issues/2) for more information.

## `map_cache.dat`

`map_cache.dat` is a keyvalue file containing map metadata. It would typically be used by online functionality in Momentum Mod.

It is entirely optional, but it adds extra metadata on the loading screen, HUD and scoreboard, such as tier and zones.

Place in your `momentum` folder.
