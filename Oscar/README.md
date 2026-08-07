# Premiações do Oscar

![Banner do projeto Oscar](./Layout/oscar%20banner.png)

Dashboard interativo sobre a história das premiações do Oscar. O relatório conecta indicações e vencedores a informações de filmes, avaliações e perfis de atores e atrizes, oferecendo diferentes caminhos de exploração.

[Voltar ao portfólio](../README.md) · [Consultar o dicionário de dados](./DATA_DICTIONARY.md)

## Visão geral

| Item | Detalhe |
| --- | --- |
| Cobertura | Filmes de 1927 a 2022; cerimônias até 2023 |
| Registros de indicações | 10.764 |
| Categorias históricas | 115 |
| Filmes distintos | 4.986 |
| Resultado | 2.438 vencedores e 8.326 indicados |
| Arquivo principal | `Oscar - Histórico.pbix` |
| Fonte local | `Database/Database.xlsx` |

## O que o dashboard permite analisar

- evolução das cerimônias e categorias ao longo do tempo;
- distribuição de indicações e vitórias;
- desempenho de filmes, atores e atrizes;
- notas, gêneros, países, bilheteria e outros atributos disponíveis para os filmes;
- detalhes de um filme ou artista selecionado.

## Páginas do relatório

1. **Início** — capa e acesso à navegação principal.
2. **Cerimônias** — indicadores, filtros e tabelas sobre indicações e vencedores.
3. **Filmes** — tendências, rankings e características das obras.
4. **Atores e atrizes** — análise de artistas indicados e premiados.
5. **Sobre** — contexto e informações do projeto.
6. **Detalhe de filmes** — visão individual da obra selecionada.
7. **Detalhe de atores** — visão individual do artista selecionado.

## Como abrir

1. Baixe esta pasta completa.
2. Abra `Oscar - Histórico.pbix` no Power BI Desktop.
3. Caso a conexão esteja quebrada, acesse **Transformar dados** no Power Query.
4. Em cada consulta que usa a planilha, atualize a etapa **Fonte** para o caminho local de `Database/Database.xlsx`.
5. Selecione **Fechar e aplicar** e atualize o relatório.

## Estrutura da base

A pasta `Database` contém uma planilha com quatro abas:

- `Filmes`: identificação e relacionamento dos filmes;
- `Detalhes_Filmes`: metadados, avaliações, elenco, receita e orçamento quando disponíveis;
- `Atores_Atrizes`: artistas, filmes, categorias, cerimônias e status de vitória;
- `Dados_Oscar`: tabela principal de indicações e vencedores.

Consulte [DATA_DICTIONARY.md](./DATA_DICTIONARY.md) para a descrição dos principais campos.

## Fonte dos dados

- Histórico das premiações: [The Oscar Award — Kaggle](https://www.kaggle.com/datasets/unanimad/the-oscar-award)
- Informações complementares de filmes presentes na base incluem identificadores e campos associados ao IMDb, Rotten Tomatoes e Metacritic.

## Limitações

- Alguns filmes não possuem nota, orçamento, receita, pôster ou outros metadados complementares.
- Categorias mudaram de nome e escopo ao longo da história; comparações entre décadas exigem contexto.
- O arquivo `.pbix` é binário e precisa do Power BI Desktop para ser explorado.

## Recursos visuais

Os ícones, imagens e demais elementos usados no layout estão em [`Layout`](./Layout/). Mantenha essa pasta ao reutilizar ou evoluir a identidade visual do relatório.
