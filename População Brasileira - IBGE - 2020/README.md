# População brasileira estimada — IBGE 2020

Dashboard interativo sobre a distribuição da população brasileira estimada em 2020. O relatório combina dados municipais, regiões, unidades federativas e coordenadas geográficas para apresentar indicadores, rankings e mapas.

[Voltar ao portfólio](../README.md) · [Consultar o dicionário de dados](./DATA_DICTIONARY.md)

## Visão geral

| Item | Detalhe |
| --- | --- |
| Referência | Estimativa populacional de 2020 |
| Municípios | 5.570 |
| Unidades federativas | 27 |
| População estimada na base | 211.755.692 habitantes |
| Arquivo principal | `População Brasileira Estimada - 2020 - IBGE.pbix` |
| Fonte local | `Database/BASES - IBGE - 2020.xlsx` |

## O que o dashboard permite analisar

- população estimada por município, estado e região;
- participação de cada localidade no total;
- municípios mais e menos populosos;
- distribuição geográfica por meio de mapa;
- comparação entre estados e regiões com filtros interativos.

O relatório possui uma página analítica com cartões, gráficos de barras e colunas, gráfico de rosca, tabelas, filtros e um mapa.

## Como abrir

1. Baixe esta pasta completa.
2. Abra `População Brasileira Estimada - 2020 - IBGE.pbix` no Power BI Desktop.
3. Caso a conexão esteja quebrada, acesse **Transformar dados** no Power Query.
4. Em cada consulta que usa a planilha, atualize a etapa **Fonte** para o caminho local de `Database/BASES - IBGE - 2020.xlsx`.
5. Selecione **Fechar e aplicar** e atualize o relatório.

## Estrutura da base

A planilha possui três abas:

- `BRASIL_E_UFs`: relação entre unidade federativa, região e sigla;
- `COORDENADAS`: latitude e longitude de referência para cada UF;
- `MUNICIPIOS`: códigos, nomes e população estimada dos 5.570 municípios.

Consulte [DATA_DICTIONARY.md](./DATA_DICTIONARY.md) para a descrição campo a campo.

## Fonte dos dados

- [Estimativas da População 2020 — IBGE](https://ftp.ibge.gov.br/Estimativas_de_Populacao/Estimativas_2020/estimativa_dou_2020.pdf)

## Limitações

- Os valores são estimativas com referência em 2020, não resultados do Censo Demográfico de 2022.
- Coordenadas representam pontos de referência das UFs e não limites geográficos.
- Comparações atuais exigem uma fonte mais recente e a atualização do modelo.
- O arquivo `.pbix` é binário e precisa do Power BI Desktop para ser explorado.
