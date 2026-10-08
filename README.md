# MODEX Data — SA-MP 0.3.7

Repositório público de dados usados pelo cliente MODEX RP para Android. O launcher carrega as listas em `data_lists/` e baixa um único pacote ZIP tanto no modo full quanto no lite.

## Pacote integrado atual — v2

O pacote público é `modex.data.zip` no release `modexdata-v2`. O manifesto usa o nome interno `modex data`, destino na raiz da pasta de dados e tamanho exato de 759.323.164 bytes. A tela do launcher oculta o nome do arquivo e mantém o progresso/contadores.

O ZIP contém 958 arquivos: os 352 arquivos da data base atual, mais 605 PNGs do catálogo de personagens e o marcador de instalação. São 1.773.454.031 bytes expandidos. SHA-256: `58ec5697ffb4601249696faac1a0d3dae8a7e5d60384ea18bc67ef1587d129f2`. A estrutura preserva os caminhos esperados pelo APK, incluindo `customcharacter/textures/`.

## Correção do crash RLE

A v2 corrige somente a cauda comprimida do registro `fist` no banco `texdb/txd/txd`: o fluxo anterior produzia 87.376 bytes, embora o cliente solicitasse 87.408, e terminava exatamente antes dos dois menores blocos de mipmap. A v2 acrescenta uma execução RLE válida usando o último bloco ETC íntegro, atualiza os comprimentos do registro e dos TOCs e valida que o fluxo completo para exatamente no tamanho solicitado. Nenhum outro conteúdo do ZIP foi alterado; `libGTASA.so` permanece byte a byte idêntica.

A comparação com `files.zip` de referência não levou à substituição dos bancos TXD: a entrada `fist` de referência usa outro formato/metadados e não é uma cópia compatível para troca direta. Os PNGs do catálogo de personagens foram preservados.

## Manifestos e atualização

`data_lists/full_list.json` e `data_lists/lite_list.json` apontam para o mesmo asset em uma única entrada `archives`; `samp_list.json` permanece vazio, portanto não há um segundo pacote de dados. O tamanho diferente da v1 invalida o marcador anterior e faz o launcher baixar a v2 uma vez.

## Releases

- v1 preservada: [`modexdata-v1`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v1)
- Atual: [`modexdata-v2`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v2)
