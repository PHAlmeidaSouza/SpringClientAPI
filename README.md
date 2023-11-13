# Projeto CRUD de Clientes usando Spring Boot

## Desafio para entrega (Trabalho final do capítulo)

### Enunciado

Projeto desenvolvido utilizando Spring Boot 3.1.5 contendo um CRUD completo de web services REST para acessar recursos de clientes. O projeto deve abranger as cinco operações básicas aprendidas no capítulo:

1. Busca paginada de recursos
2. Busca de recurso por ID
3. Inserção de novo recurso
4. Atualização de recurso
5. Exclusão de recurso

### Requisitos

O projeto deve atender aos seguintes requisitos:

- Utilizar o ambiente de testes configurado, acessando o banco de dados H2.
- Utilizar o Maven como gerenciador de dependências.
- Utilizar Java 17+ como linguagem.

### Entidade Client

Um cliente possui os seguintes atributos: nome, CPF, renda, data de nascimento e quantidade de filhos. A especificação da entidade `Client` é detalhada a seguir (é crucial seguir exatamente os nomes de classe e atributos apresentados no diagrama).

### Seed de Dados

O projeto deve conter um seed de pelo menos 10 clientes com dados SIGNIFICATIVOS, evitando o uso de dados sem significado como "Nome 1", "Nome 2", etc.

### Observações Importantes

- Crie um novo projeto exclusivamente para este trabalho, evitando simplesmente adicionar a classe `Client` ao DSCatalog feito nas aulas.
- Lembre-se de que, por padrão, a JPA transforma nomes de atributos de camelCase para snake_case. Por exemplo, o campo `birthDate` será criado no banco de dados como `birth_Date`. Portanto, o script SQL deve seguir esse padrão.
- Tome cuidado para não salvar no seu projeto arquivos e pastas que não devem ser incluídos no Git, como a pasta `.metadata` do Eclipse.

### Critérios de Correção

1. **Importação do Projeto:**
   - O professor deve conseguir clonar o projeto do GitHub e importá-lo no STS sem a necessidade de configurações especiais além daquelas já ensinadas em aula.

2. **Testes Manuais no Postman:**
   - O professor já preparou as requisições Postman listadas abaixo. Todas elas devem funcionar corretamente para validar o correto funcionamento do sistema:

   - **Busca paginada de clientes:**
     ```
     GET /clients?page=0&linesPerPage=6&direction=ASC&orderBy=name
     ```

   - **Busca de cliente por ID:**
     ```
     GET /clients/1
     ```

   - **Inserção de novo cliente:**
     ```
     POST /clients
     {
       "name": "Maria Silva",
       "cpf": "12345678901",
       "income": 6500.0,
       "birthDate": "1994-07-20T10:30:00Z",
       "children": 2
     }
     ```

   - **Atualização de cliente:**
     ```
     PUT /clients/1
     {
       "name": "Maria Silvaaa",
       "cpf": "12345678901",
       "income": 6500.0,
       "birthDate": "1994-07-20T10:30:00Z",
       "children": 2
     }
     ```

   - **Exclusão de cliente:**
     ```
     DELETE /clients/1
     ```
