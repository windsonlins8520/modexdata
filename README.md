# MODEX Data — SA-MP 0.3.7

Repositório público dos arquivos de Data usados pelo cliente MODEX RP para Android. O launcher lê os manifestos em `data_lists/` e baixa o pacote ZIP pelos modos full e lite.

## Versão atual — v10 nativa

- **Download:** [`modex.data.v10.native.zip`](https://github.com/windsonlins8520/modexdata/releases/download/modexdata-v10-native/modex.data.v10.native.zip)
- **Release:** [MODEX Data v10 — SA-MP nativa](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v10-native)
- **Tamanho:** 617.019.857 bytes
- **SHA-256:** `8ac4c967e92a45014281f5f132a2e398e653060fad2c8ccfca25f7ea01def49a`

A v10 restaura a Data ao baseline nativo (`Nativo.zip`). Seus 352 arquivos têm nomes, tamanhos e CRCs idênticos ao baseline verificado. Não contém os assets customizados do criador nem modificações MODEX de skins, veículos, mapa/minimapa, HUD ou velocímetro.

A v8 nativa permanece preservada no histórico; a v10 republica o mesmo conteúdo stock sob uma versão nova para que seja a versão atual e os manifests baixem o pacote correto. A v9 Creator e as demais releases antigas são apenas históricas e não são usadas pelos manifests atuais.

## Arquivos distribuídos

- `data_lists/full_list.json` e `data_lists/lite_list.json` apontam para a v10 nativa.
- `data_lists/samp_list.json` permanece vazio, como antes.
- `update.json` mantém `game_version` **1.0.78**; a versão do launcher não foi alterada.

**Este repositório publica somente a Data.** APKs não são anexados ao GitHub e continuam fora deste repositório. A GameMode não foi modificada nem incluída na release.

## Integridade

O ZIP passou no teste CRC. A comparação direta confirmou igualdade dos 352 arquivos com o baseline `Nativo.zip` por nome, tamanho e CRC. Isso verifica a correspondência do pacote; não substitui o teste em um aparelho e servidor reais.

## Releases anteriores

- [v1 — pacote integrado](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v1)
- [v2 — correção RLE de `fist`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v2)
- [v3 — correção RLE de `leather_seat`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v3)
- [v5 — correções de streams RLE](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v5)
- [v6 — validação de bancos mobile/txd](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v6)
- [v7 — Data modificada](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v7)
- [v8 — Data stock/nativa](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v8-native)
- [v9 — Data com assets do criador (histórica)](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v9-creator)
