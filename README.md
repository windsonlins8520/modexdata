# MODEX Data — SA-MP 0.3.7

Repositório público de dados usados pelo cliente MODEX RP para Android. O launcher lê os manifestos em `data_lists/` e baixa um único pacote ZIP tanto no modo full quanto no lite.

## Pacote publicado — v5

O pacote publicado é `modex.data.v5.zip`, na tag [`modexdata-v5`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v5). Tamanho exato: **772.487.701 bytes**. SHA-256: `0b751fe3b01094b20a85a2da568860e1c177b7f528d7dbf7db30b5fdc3bffed8`.

O ZIP mantém os 958 arquivos e os caminhos esperados pelo APK, incluindo `customcharacter/textures/`. Apenas os três DAT e os três TOCs do banco `texdb/gta3` mudaram em relação ao candidato v4 local. Os pacotes públicos v1, v2 e v3 permanecem preservados; o v4 intermediário não foi publicado e foi substituído por esta correção mais abrangente.

## Correções RLE

A v2 corrigiu a cauda comprimida da textura `fist` no banco `texdb/txd/txd`. A v3 manteve essa correção e reparou `leather_seat` nos bancos `texdb/gta3/gta3.{dxt,etc,pvr}.dat`. A candidata v4 local corrigiu `carpet`, identificada no diagnóstico da APK 1.0.78 no offset `0x09F91BB0`.

Depois da correção de `carpet`, uma auditoria que espelha o limite de destino e o tamanho de bloco de `RLEDecompress` nativo percorreu os **10.367 registros** do banco GTA3. Ela encontrou **1.052 fluxos que não alcançavam a saída solicitada**: 947 terminavam entre blocos completos e 105 acabavam no meio de um token. O pacote v5 preserva os blocos válidos, remove qualquer token final incompleto e completa a cauda com um run RLE válido baseado no último bloco decodificado (ou bloco zero quando não havia bloco anterior).

Após o reparo, os bancos DXT, ETC e PVR foram auditados novamente: **0 underflows e 0 tokens incompletos** nos 10.367 registros de cada variante. Os 742 casos de arredondamento do último bloco permanecem como comportamento do decodificador nativo quando o tamanho destino não é múltiplo do bloco; não foram classificados como streams curtos. A correção de `fist` continua válida. O ZIP passou no teste de integridade; o reparo adiciona 11.104 bytes de runs RLE e descarta 462 bytes de tokens truncados.

## Manifestos e impacto da atualização

Os manifestos públicos `full_list.json` e `lite_list.json` apontam para o pacote v5; `samp_list.json` permanece inalterado. O manifesto público `update.json` declara `game_version` `1.0.78`.

A mudança v3→v5 faz instalações existentes baixarem novamente o pacote completo de aproximadamente **737 MiB** (772.487.701 bytes). O endpoint do asset é `https://github.com/windsonlins8520/modexdata/releases/download/modexdata-v5/modex.data.v5.zip`.

## Releases

- v1 preservada: [`modexdata-v1`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v1)
- v2 preservada: [`modexdata-v2`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v2)
- v3 preservada: [`modexdata-v3`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v3)
- v5 publicada: [`modexdata-v5`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v5)
