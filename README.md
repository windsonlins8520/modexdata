# Nativo — SA-MP 0.3.7 game data and custom character assets

Public data repository for the Nativo Android client. The release assets are downloaded by the launcher through `data_lists/full_list.json` and `data_lists/lite_list.json`.

## Release assets

- `Nativo.zip`: copy of the authorized game-data archive; the archive's internal content is preserved. Its launcher display name is `Nativo`.
- `Nativo_CustomCharacter_Update.zip`: 605 PNG assets for the custom character panel, extracted under `customcharacter/textures/`.

The manifest files include both archives in full and lite modes. `update.json` remains version `17.0` and points to this repository's raw manifests. The custom character system remains SA-MP 0.3.7; no DL-only custom model RPCs are used.

## Status

The public repository, manifests, and release assets are published. Release URL: https://github.com/windsonlins8520/Nativo.zip/releases/tag/nativo-v1

- `Nativo.zip` SHA-256: `8ac4c967e92a45014281f5f132a2e398e653060fad2c8ccfca25f7ea01def49a`.
- `Nativo_CustomCharacter_Update.zip` SHA-256: `8bfdf2925dc35f2ee5a1aaaa90c0190c7360ad9619813b8b8eb4ed6309c560d4`.
