Testes de API – Hub de Leitura
Sobre o projeto

Este diretório reúne os artefatos de testes de API desenvolvidos como parte do exercício prático do curso de QA da EBAC.

O objetivo é validar a funcionalidade Catálogo de Livros, verificando o comportamento dos endpoints, os códigos HTTP, as regras de negócio e o tratamento de entradas inválidas.

Ferramentas utilizadas
Postman – execução e validação das requisições.
JavaScript – criação de asserções.
Swagger – consulta à documentação da API.
Escopo dos testes

Foram utilizados os métodos HTTP:

GET – consulta e listagem de livros.
POST – cadastro de livros.
PUT – atualização de livros.
DELETE – exclusão de livros.

Também foram considerados cenários negativos, incluindo consulta de livro inexistente e tentativa de cadastro com campos obrigatórios vazios.

Estrutura
casos-de-teste.md: documentação dos cenários.
postman/: Collection de testes exportada em JSON.
Observações e oportunidades de melhoria

Durante a execução dos testes da funcionalidade Catálogo de Livros, foram identificadas duas oportunidades de melhoria:

1. Retorno de erros de validação

Ao enviar uma requisição POST com múltiplos campos vazios, a API retornou somente o primeiro campo inválido (title).

Sugestão: avaliar a possibilidade de retornar todos os campos que apresentam erros de validação em uma única resposta.

2. Padronização das mensagens de resposta

Foram observadas mensagens de retorno em português e inglês.

Sugestão: estabelecer um padrão único para as mensagens, preferencialmente em português, mantendo os códigos técnicos de erro em inglês.

Essas observações não representam necessariamente defeitos funcionais, mas oportunidades de melhoria na consistência da API e na experiência dos consumidores.