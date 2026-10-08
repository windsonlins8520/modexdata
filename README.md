# MODEX Data — SA-MP 0.3.7

Repositório público de dados usados pelo cliente MODEX RP para Android. O launcher lê os manifestos em `data_lists/` e baixa um único pacote ZIP tanto no modo full quanto no lite.

## Pacote integrado atual — v3

O asset público é [`modex.data.v3.zip`](https://github.com/windsonlins8520/modexdata/releases/download/modexdata-v3/modex.data.v3.zip) no release [`modexdata-v3`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v3). O manifesto usa o nome interno `modex data`, destino na raiz da pasta de dados e tamanho exato de **772.471.627 bytes**. SHA-256: `ddd54ebd2d087abc1934bb3f9416fb73eb824275b1851d2695b57cf799b70519`.

O ZIP contém 958 arquivos e 1.773.454.061 bytes expandidos: os dados base do jogo, os PNGs do catálogo de personagens e o marcador de instalação, preservando os caminhos esperados pelo APK, incluindo `customcharacter/textures/`.

## Correções de textura RLE

A v2 corrigiu a cauda comprimida da textura `fist` no banco `texdb/txd/txd`; a v3 mantém essa correção e também corrige a textura `leather_seat` nos bancos `texdb/gta3/gta3.dxt.dat`, `gta3.etc.dat` e `gta3.pvr.dat`. Em cada variante, o fluxo RLE anterior terminava 24 bytes antes do tamanho esperado de 87.400 bytes. A v3 acrescenta uma execução RLE válida e atualiza os comprimentos do registro e os offsets dos TOCs correspondentes.

A validação confirma que o fluxo passa a produzir o tamanho solicitado, que a correção anterior de `fist` continua válida e que o ZIP completo é íntegro. A comparação entre v2 e v3 encontrou alterações somente nos três arquivos DAT e nos três TOCs correspondentes; os outros membros foram preservados.

O ZIP v3 tem 13.148.463 bytes a mais que o v2 por causa da recompressão dos registros modificados; o conteúdo expandido aumentou apenas 30 bytes no total (10 bytes codificados em cada uma das três variantes gráficas).

## Manifestos e atualização

`data_lists/full_list.json` e `data_lists/lite_list.json` apontam para o mesmo asset v3 em uma única entrada `archives`; `samp_list.json` permanece inalterado. A mudança de tamanho invalida o marcador v2 do launcher e solicita a instalação do pacote atualizado uma vez.

## Releases

- v1 preservada: [`modexdata-v1`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v1)
- v2 preservada: [`modexdata-v2`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v2)
- Atual: [`modexdata-v3`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v3)
