# Basic AntiCheat for Valheim

Bepinex plugin for Valheim that prevents players from connecting to your server with mismatching plugins loaded.
Needs to be present on both, client and server.
You can still connect to servers not running the plugin.

## Usage

- Install to client and server
- Make sure client and server mods in the `plugins` folder are identical

## Configuration

- Coming soon

## Installation (manual)

If you are installing this manually, do the following

- Download [BepInEx Package](https://valheim.thunderstore.io/package/denikson/BepInExPack_Valheim/) and follow it's installation procedure.
- Download AntiCheat
- Extract the contents of `plugins` folder into `<GameDirectory>\Bepinex\plugins`.
- Run the game/server

## Planned

- Configurable plugin configuration verification
- Allow whitelisting of specific mods on the server
- Properly handshake before verification (RPC)
- API for 3rd party plugins

## Changelog
0.1.1
- Update this readme
0.1.0
- Initial release
