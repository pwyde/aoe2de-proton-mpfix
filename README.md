# Multiplayer fix for Age of Empires II: Definitive Edition
This script fixes multiplayer "Out of sync" error in **[Age of Empires II: Definitive Edition](https://store.steampowered.com/app/813780/Age_of_Empires_II_Definitive_Edition/)** using Proton.
It will check if `ucrtbase.dll` is installed and installs it if necessary. Set the Steam launch options below
to run it automatically before launching the game.

```
/path/to/script/run.sh ; %command% %steam_location%
```

For example, if repo is cloned to the `$HOME/.local/share` directory, then set launch option to the following:

```
~/.local/share/aoe2de-proton-mpfix/run.sh ; %command% %steam_location%
```

If `%steam_location%` is not set, the script will default to `$HOME/.local/share`.

## Dependencies
- **[cabextract](https://archlinux.org/packages/?name=cabextract)**: Required to extract `ucrtbase.dll` from the downloaded `vc_redist.x64.exe` file.
- **[wget](https://archlinux.org/packages/?name=wget)**: Required for downloading `vc_redist.x64.exe` from Microsoft.
- **[jq](https://archlinux.org/packages/?name=jq)**: Required to automatically fetch Steam App ID (Optional).
