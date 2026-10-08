# Nativo — SA-MP 0.3.7 game data and custom character assets

Public data repository for the Nativo Android client. The release assets are downloaded by the launcher through `data_lists/full_list.json` and `data_lists/lite_list.json`.

## Release assets

- `Nativo.zip`: copy of the authorized game-data archive; the archive's internal content is preserved. Its launcher display name is `Nativo`.
- `Nativo_CustomCharacter_Update.zip`: 605 PNG assets for the custom character panel, extracted under `customcharacter/textures/`.

The manifest files include both archives in full and lite modes. `update.json` remains version `17.0` and points to this repository's raw manifests. The custom character system remains SA-MP 0.3.7; no DL-only custom model RPCs are used.

## Status

Repository seed files are prepared locally. Publishing them requires GitHub write permission for repository creation, contents, and release assets.
