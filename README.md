# MODEX Data — SA-MP 0.3.7

Repositório público de dados usados pelo cliente MODEX RP para Android. O launcher lê os manifestos em `data_lists/` e baixa o pacote ZIP nos modos full e lite.

## Pacote atual — v7

- Download: [`modex.data.v7.zip`](https://github.com/windsonlins8520/modexdata/releases/download/modexdata-v7/modex.data.v7.zip)
- Release: [`modexdata-v7`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v7)
- Tamanho: **775.448.929 bytes** (aprox. 739 MiB)
- SHA-256: `16273c21a6121c8f9fe90fd1f312f71fbfce292a58f3da53e6d6df4e4570d844`

A v7 restaura skins, HUD, menus, controles e punho para o visual padrão, removendo o velocímetro e as alterações visuais de skins/interfaces. Mantém o mapa escuro/GTA V do minimapa, os mods de veículos e os 606 arquivos de `customcharacter`. Os modelos male/female (`male.dff/.txd` e `female.dff/.txd`) estão no APK, nos slots 7 e 9, e não duplicados neste ZIP.

## Integridade e estabilidade

O pacote passou pela verificação integral de CRC do ZIP. Na reconstrução, só foram mantidas caudas RLE do v6 quando os bytes anteriores do registro permaneciam idênticos; isso preserva os reparos de streams sem reaplicar alterações visuais não desejadas. Foram conservados 117 nomes de texturas de veículos, 212 entradas de modelo e os índices do minimapa escuro.

**Ressalva de validação:** o modelo de veículo `tropic.dff`, herdado da Data de origem, não foi modificado. Um parser offline sinalizou EOF ao ler um campo de geometria; isso não comprova falha em execução no jogo, mas o pacote ainda precisa de teste em cliente Android real para certificar o comportamento em runtime.

## Manifestos e atualização

`full_list.json` e `lite_list.json` apontam para a v7. `samp_list.json` permanece sem alteração. `update.json` mantém `game_version` **1.0.78**, correspondente ao `versionName` do APK DEBUG construído; os URLs dos manifestos são estáveis e agora servem a nova lista.

O APK universal DEBUG é entregue separadamente e não faz parte desta release do Data. É destinado a teste/instalação manual, não substitui um APK de produção assinado com a chave original do aplicativo.

## Releases preservadas

- [v1 — pacote integrado](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v1)
- [v2 — correção RLE de `fist`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v2)
- [v3 — correção RLE de `leather_seat`](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v3)
- [v5 — correções de streams RLE](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v5)
- [v6 — validação de bancos mobile/txd](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v6)
- [v7 — base limpa, mapa escuro e customização preservados](https://github.com/windsonlins8520/modexdata/releases/tag/modexdata-v7)
