# MODEX Data — SA-MP 0.3.7

Repositório público de dados usados pelo cliente MODEX RP para Android. O launcher lê os manifestos em `data_lists/` e baixa o pacote ZIP nos modos full e lite.

## Pacote atual — v9 Creator

- Download: [`modex.data.v9.creator.zip`](https://github.com/windsonlins8520/modexdata/releases/download/modexdata-v9-creator/modex.data.v9.creator.zip)
- Release: [`modexdata-v9-creator`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v9-creator)
- Tamanho: **749.499.435 bytes**
- SHA-256: `ba99c37af554e3167f9cfbca5eb7e3ef8506b321186015d30af03e5874573d7e`

A v9 usa a Data stock v8 como base e acrescenta somente 503 texturas PNG do catálogo `customcharacter/textures/10` e `customcharacter/textures/14`, para rosto, cabelo, roupas, calçados e corpo. Os arquivos da base v8 foram preservados com CRC/tamanho idênticos. Não foram incluídos os antigos mods de mapa/minimapa, veículos, velocímetro ou HUD.

## Compatibilidade do criador

A Data v9 é destinada ao APK MODEX Creator v2. O cliente oferece dados de cadastro, escolha de gênero e opções visuais que existem no catálogo instalado. O modelo masculino atualmente não tem opções próprias de cabelo/calçados nesse catálogo; esses controles são mostrados para o modelo feminino. Tatuagens, barba e sobrancelhas do recurso MTA não foram integradas nesta versão: o formato do MTA não é carregado diretamente pelo SA-MP 0.3.7 e requer uma camada de renderização/ativos próprios.

O APK **não** é distribuído neste repositório; permanece disponível apenas por links diretos de download separados. A GameMode também não é anexada à release da Data.

## Integridade e compatibilidade

O ZIP passou pela verificação CRC integral. A comparação do conteúdo confirma que todos os 352 arquivos da base v8 permanecem inalterados e que os únicos arquivos adicionados são as texturas do criador. Isso verifica a integridade do pacote, mas não substitui um teste em dispositivo Android real nem garante ausência de travamentos em todo aparelho/servidor.

## Manifestos

- `data_lists/full_list.json` e `data_lists/lite_list.json` apontam para a release v9.
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
- [v9 — Data stock com assets do criador](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v9-creator)
