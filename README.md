# MODEX Data — SA-MP 0.3.7

Repositório público de dados usados pelo cliente MODEX RP para Android. O launcher carrega as listas em `data_lists/` e baixa um único pacote ZIP tanto no modo full quanto no lite.

## Pacote integrado

O pacote local foi gerado como `modex data.zip`. Na publicação, o GitHub normalizou o espaço para ponto; o nome efetivo do asset é `modex.data.zip`. O manifesto usa o nome interno `modex data`, portanto o arquivo temporário do APK mantém esse nome, embora a tela de download não o mostre.

O ZIP contém 958 arquivos: os 352 arquivos da data base atual, mais 605 PNGs do catálogo de personagens e o marcador de instalação. São 1.773.453.977 bytes expandidos e 758.743.438 bytes compactados. SHA-256: `369c9669f9c4da41b93e47d321343bf6abfa19b2d6bc26ef45b6c9f29f3f3566`. A estrutura preserva os caminhos esperados pelo APK, incluindo `customcharacter/textures/`.

O pacote foi construído a partir dos dois assets atuais já publicados e autorizados. Não foram adicionados os 257 PNGs exclusivos do `files.zip` de referência, os DFF/TXD incompatíveis nem os bancos `texdb` divergentes. O conteúdo mantém compatibilidade com SA-MP 0.3.7 e não usa recursos de 0.3.DL.

## Manifestos e atualização

`data_lists/full_list.json` e `data_lists/lite_list.json` apontam para o mesmo asset em uma única entrada `archives`; `update.json` aponta para os manifestos usando o repositório `windsonlins8520/modexdata`. A entrada do pacote tem destino relativo vazio (raiz da pasta de dados) e tamanho exato de 758.743.438 bytes.

Quem já tem os pacotes anteriores fará uma atualização única do pacote completo, porque o manifesto passa de dois arquivos para um asset integrado. Depois, o marcador do ZIP evita repetir o download enquanto o manifesto e o tamanho permanecerem iguais.

## Release publicado

Tag: [`modexdata-v1`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v1). Asset: [`modex.data.zip`](https://github.com/windsonlins8520/modexdata/releases/download/modexdata-v1/modex.data.zip).
