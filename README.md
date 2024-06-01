## 🔖 Sobre

# Screenmatch With Spring Boot

Screenmatch é uma aplicação desenvolvida em Java com o objetivo de buscar, listar e armazenar informações sobre séries e seus episódios. Utilizando a API OMDb, a aplicação permite realizar diversas consultas e interações com os dados das séries.

## Funcionalidades

- Buscar séries e episódios online.
- Listar séries buscadas.
- Buscar séries por nome, ator, categoria, número de temporadas, entre outros critérios.
- Exibir o top 5 de séries e episódios.
- Armazenar informações das séries e episódios em um banco de dados.

## Tecnologias Utilizadas

- **Java**: Linguagem de programação principal.
- **Spring Boot**: Framework para facilitar o desenvolvimento da aplicação.
- **Spring Data JPA**: Para gerenciamento de persistência e consultas ao banco de dados.
- **OMDb API**: API utilizada para buscar informações sobre séries.
- **OpenAI API**: Utilizada para traduções via GPT-3.5-turbo.
- **Jackson**: Biblioteca para manipulação de JSON.
- **HTTP Client**: Para consumo da API externa.

## Estrutura do Projeto

### `ScreenmatchApplication`

Classe principal da aplicação que inicializa o Spring Boot e executa o método `run` ao iniciar.

### `Principal`

Classe responsável por exibir o menu e gerenciar as interações do usuário. Contém métodos para:
- Buscar séries e episódios.
- Listar séries buscadas.
- Buscar séries por diferentes critérios.
- Exibir o top 5 de séries e episódios.

### Modelos

#### `Categoria`
Enumeração que define as categorias das séries, com suporte para tradução de inglês para português.

#### `DadosEpisodio`
Classe para representar os dados dos episódios recebidos da API.

#### `DadosSerie`
Classe para representar os dados das séries recebidos da API.

#### `DadosTemporada`
Classe para representar os dados das temporadas, incluindo uma lista de episódios.

#### `Episodio`
Entidade JPA que mapeia os episódios no banco de dados.

#### `Serie`
Entidade JPA que mapeia as séries no banco de dados. Inclui métodos para manipulação e apresentação dos dados da série.

### Repositórios

#### `SerieRepository`
Interface que estende `JpaRepository`, fornecendo métodos para operações CRUD e consultas customizadas no banco de dados.

### Serviços

#### `ConsultaChatGPT`
Classe responsável por interagir com a API do OpenAI para obter traduções.

#### `ConsumoApi`
Classe que faz as requisições HTTP para a API do OMDb e retorna os dados em formato JSON.

#### `ConverteDados`
Classe que utiliza a biblioteca Jackson para converter JSON em objetos Java.

# Desenvolvedor

[<img loading="lazy" src="https://avatars.githubusercontent.com/u/134724019?v=4" width=115><br><sub>Ronaldo Navarro</sub>](https://github.com/ronaldosnavarro)
