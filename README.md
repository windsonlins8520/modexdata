# MODEX Data — SA-MP 0.3.7

Repositório público de dados usados pelo cliente MODEX RP para Android. O launcher lê os manifestos em `data_lists/` e baixa o pacote ZIP nos modos full e lite.

## Pacote atual — v8 nativa

- Download: [`modex.data.v8.native.zip`](https://github.com/windsonlins8520/modexdata/releases/download/modexdata-v8-native/modex.data.v8.native.zip)
- Release: [`modexdata-v8-native`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v8-native)
- Tamanho: **617.019.857 bytes** (aprox. 588,5 MiB)
- SHA-256: `8ac4c967e92a45014281f5f132a2e398e653060fad2c8ccfca25f7ea01def49a`

A v8 usa a Data-base original (`Nativo.zip`) sem mesclar alterações da v7: não inclui overrides de skins/personagens, veículos modificados, mapa escuro/minimapa GTA V, velocímetro, HUD customizado ou pacote de texturas `customcharacter`. O visual de jogo fica a cargo dos recursos nativos do SA-MP/GTASA.

## Integridade e compatibilidade

O ZIP foi conferido integralmente (`unzip -t`) e corresponde byte a byte ao arquivo-base stock disponível no projeto. Isso valida a integridade do arquivo, mas não substitui um teste em dispositivo Android real nem permite garantir ausência de travamentos em toda combinação de aparelho/servidor.

O APK DEBUG nativo é distribuído separadamente para instalação manual; não está anexado à release pública da Data. A GameMode permanece inalterada nesta revisão: mensagens, textdraws, diálogos e regras enviados pelo servidor continuam sob responsabilidade da GameMode instalada na host.

## Manifestos

- `data_lists/full_list.json` e `data_lists/lite_list.json` apontam para a release v8.
- `data_lists/samp_list.json` permanece sem alteração.
- `update.json` conserva `game_version` **1.0.78**; o número da versão do launcher não mudou.

## Releases anteriores preservadas

- [v1 — pacote integrado](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v1)
- [v2 — correção RLE de `fist`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v2)
- [v3 — correção RLE de `leather_seat`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v3)
- [v5 — correções de streams RLE](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v5)
- [v6 — validação de bancos mobile/txd](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v6)
- [v7 — Data com minimapa escuro, veículos e customização](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v7)
- [v8 — Data stock/nativa](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v8-native)
