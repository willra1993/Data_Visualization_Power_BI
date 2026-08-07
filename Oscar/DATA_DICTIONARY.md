# Dicionário de dados — Oscar

[Voltar à documentação do projeto](./README.md)

O arquivo `Database/Database.xlsx` possui quatro abas relacionadas. As contagens abaixo consideram a versão atualmente incluída no repositório.

## `Dados_Oscar`

Tabela principal com 10.764 registros de indicações e premiações.

| Campo | Descrição |
| --- | --- |
| `year_film` | Ano de lançamento do filme |
| `year_ceremony` | Ano da cerimônia |
| `ceremony` | Número da edição da cerimônia |
| `category` | Categoria da indicação |
| `name` | Pessoa, filme ou obra indicada, conforme a categoria |
| `film` | Filme associado à indicação, quando aplicável |
| `winner` | Indicador de vitória na fonte original |
| `Filme_Ano` | Chave composta por filme e ano |
| `Década` | Faixa de década derivada do ano do filme |
| `Status` | Classificação amigável: `Indicado` ou `Vencedor` |

## `Filmes`

Tabela de relacionamento com 5.080 filmes.

| Campo | Descrição |
| --- | --- |
| `FIlme_Ano` | Chave composta original para relacionamento |
| `Nome_IMDB` | Título correspondente no IMDb |
| `IMDB_ID` | Identificador do título no IMDb |
| `Ano` | Ano do filme |
| `NomeIMDB_Ano` | Chave composta com o título padronizado e o ano |

## `Detalhes_Filmes`

Tabela com 5.080 linhas e 31 campos de metadados. Os grupos principais são:

| Grupo | Campos principais |
| --- | --- |
| Identificação | `Title`, `Year`, `imdbID`, `Type`, `Nome_Ano` |
| Conteúdo | `Genre`, `Director`, `Writer`, `Actors`, `Plot`, `Language`, `Country` |
| Lançamento | `Rated`, `Released`, `Runtime`, `DVD` |
| Avaliações | `Metascore`, `imdbRating`, `imdbVotes`, `Internet Movie Database`, `Rotten Tomatoes`, `Metacritic` |
| Resultado comercial | `BoxOffice`, `budget`, `revenue`, `Production` |
| Recursos externos | `Poster`, `Website` |

Valores ausentes podem aparecer como células vazias ou `N/A`, dependendo da fonte.

## `Atores_Atrizes`

Tabela com 1.808 registros relacionados a intérpretes.

| Campo | Descrição |
| --- | --- |
| `Filme_Ano` | Chave composta do filme e ano |
| `name` | Nome do ator ou da atriz |
| `URL` | Endereço da imagem de perfil, quando disponível |
| `film` | Filme associado à indicação |
| `year_film` | Ano do filme |
| `year_ceremony` | Ano da cerimônia |
| `ceremony` | Número da edição da cerimônia |
| `category` | Categoria de atuação |
| `winner` | Indicador de vitória |

## Relacionamentos esperados

- `Dados_Oscar[Filme_Ano]` → `Filmes[FIlme_Ano]`
- `Filmes[NomeIMDB_Ano]` → `Detalhes_Filmes[Nome_Ano]`
- `Dados_Oscar[Filme_Ano]` → `Atores_Atrizes[Filme_Ano]`, conforme o contexto de análise

> As chaves compostas devem ser revisadas ao atualizar as fontes, pois diferenças de título ou ano podem impedir correspondências.
