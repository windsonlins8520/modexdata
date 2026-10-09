# MODEX Data — SA-MP 0.3.7

Repositório público de dados usados pelo cliente MODEX RP para Android. O launcher lê os manifestos em `data_lists/` e baixa um único pacote ZIP tanto no modo full quanto no lite.

## Pacote publicado — v6

O pacote publicado é `modex.data.v6.zip`, na tag [`modexdata-v6`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v6). Tamanho exato: **772.850.305 bytes**. SHA-256: `1eb38acb96f439bf70d1fbfdb4351f48faa8e2a1dc315d3cbda57185a3be268f`.

O ZIP preserva os 958 arquivos, os caminhos esperados pelo APK e todas as correções anteriores. Em relação à v5, somente os DAT e TOC dos bancos `texdb/mobile` e `texdb/txd` foram atualizados; os nomes das texturas, os manifestos de conteúdo e as bibliotecas nativas não foram modificados.

## Correções RLE

A v2 corrigiu a cauda comprimida da textura `fist` no banco `texdb/txd/txd`. A v3 manteve essa correção e reparou `leather_seat` nos bancos GTA3. A v5 corrigiu `carpet` e outros fluxos incompletos: uma auditoria nativa percorreu **10.367 registros** do GTA3 e reparou **1.052 streams** nas variantes DXT, ETC e PVR.

A investigação do crash ao pressionar **Entrar/Registrar** identificou `hud_stinger`, no banco `mobile`, como um RLE que parava **32 bytes** antes do tamanho de saída esperado. A auditoria completa do pacote v5 encontrou **374 fluxos incompletos** nas variantes Android: 120 registros no `mobile.dxt`, 118 em `mobile.etc`, 118 em `mobile.pvr` e 6 em cada variante do banco `txd`. Esses registros correspondem a **120 índices de textura distintos em mobile** (dois presentes apenas em DXT) e **6 índices em txd**.

A v6 preserva cada prefixo RLE válido, remove somente caudas/tokens incompletos e completa as saídas com runs RLE válidos. Após a correção, a auditoria espelhando o tamanho de bloco e o limite de destino nativos verificou **2.211 registros** nos bancos mobile/txd: **zero underflows e zero tokens incompletos** em DXT, ETC e PVR. Os arredondamentos de último bloco já observados permanecem como comportamento do decodificador nativo, não como fluxos truncados.

## Manifestos e atualização

Os manifestos públicos `full_list.json` e `lite_list.json` apontam para a v6. O `samp_list.json` permanece inalterado; `update.json` continua declarando `game_version` **1.0.78**. Instalações que já baixaram a v5 precisarão baixar novamente o pacote de dados completo (772.850.305 bytes, cerca de 737 MiB).

## Releases

- v1 preservada: [`modexdata-v1`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v1)
- v2 preservada: [`modexdata-v2`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v2)
- v3 preservada: [`modexdata-v3`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v3)
- v5 preservada: [`modexdata-v5`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v5)
- v6 publicada: [`modexdata-v6`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v6)
