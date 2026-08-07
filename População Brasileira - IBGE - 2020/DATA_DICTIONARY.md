# Dicionário de dados — população brasileira

[Voltar à documentação do projeto](./README.md)

O arquivo `Database/BASES - IBGE - 2020.xlsx` possui três abas estruturadas.

## `MUNICIPIOS`

Tabela principal com 5.570 municípios.

| Campo | Descrição |
| --- | --- |
| `UF` | Sigla da unidade federativa |
| `COD. UF` | Código numérico da unidade federativa |
| `COD. MUNIC` | Código do município na base |
| `NOME DO MUNICÍPIO` | Nome do município |
| `POPULAÇÃO ESTIMADA` | População estimada para 2020 |

## `BRASIL_E_UFs`

Dimensão com as 27 unidades federativas.

| Campo | Descrição |
| --- | --- |
| `UNIDADE FEDERATIVA` | Nome completo do estado ou do Distrito Federal |
| `REGIÃO` | Região geográfica do Brasil |
| `UF` | Sigla usada no relacionamento com as demais tabelas |

## `COORDENADAS`

Tabela auxiliar com um ponto geográfico de referência por UF.

| Campo | Descrição |
| --- | --- |
| `UF` | Sigla da unidade federativa |
| `Latitude` | Latitude do ponto de referência |
| `Longitude` | Longitude do ponto de referência |

## Relacionamentos esperados

- `MUNICIPIOS[UF]` → `BRASIL_E_UFs[UF]`
- `MUNICIPIOS[UF]` → `COORDENADAS[UF]`

## Controles de qualidade recomendados

- validar a presença das 27 UFs;
- confirmar que cada município possui população numérica e positiva;
- remover espaços antes ou depois das siglas de UF ao atualizar a base;
- conferir se o total populacional permanece consistente com a publicação de referência;
- documentar mudanças de código ou nome de municípios em novas versões.
