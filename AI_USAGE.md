# Registro de Uso de IA Generativa

## Avaliação A1 - Módulo de Produtos

Durante o desenvolvimento da Avaliação A1 do Módulo de Produtos da SocialConnect API, utilizei as ferramentas de inteligência artificial generativa **Gemini (Google)** e **Claude (Anthropic)** como apoio técnico e produtividade para a elaboração de partes específicas do projeto:

1. **Definição de DTOs e Validações:**
   O Gemini e o Claude foram utilizados para auxiliar na estruturação inicial das classes de transferência de dados (`ProdutoRequestDTO` e `ProdutoResponseDTO`) com a sintaxe de records do Java 21, além da aplicação de anotações do Jakarta Bean Validation (`@NotBlank`, `@NotNull`, `@Size`) e elaboração de validações customizadas.

2. **Documentação com Swagger/OpenAPI:**
   Utilizei as ferramentas para agilizar o mapeamento das anotações do SpringDoc OpenAPI nos endpoints do `ProdutoController` e nos atributos dos DTOs, definindo descrições, sumários, os diferentes códigos de retorno HTTP da API REST (200, 201, 204, 400, 404, 409 e 422) e exemplos práticos por meio da anotação `@Schema(example = "...")`.

3. **Padronização de Erros (RFC 7807):**
   As IAs serviram de consulta para a montagem da estrutura de tratamento de exceções com `GlobalExceptionHandler` e `ProblemDetail`, assegurando respostas ricas e detalhadas para regras de negócio, como o retorno HTTP 422 (Unprocessable Entity) para tentativas de estoque negativo e HTTP 409 (Conflict) para nomes duplicados.

4. **Geração dos Testes Automatizados:**
   Toda a parte de testes automatizados do módulo de produtos foi gerada com o auxílio do Gemini e Claude. Isso inclui tanto os testes unitários da camada de serviço (`ProdutoServiceTest`) utilizando JUnit 5 e Mockito estruturados segundo o padrão AAA (Arrange, Act, Assert), quanto a configuração dos testes de integração (`ProdutoControllerIntegrationTest`) utilizando Testcontainers e PostgreSQL 17.