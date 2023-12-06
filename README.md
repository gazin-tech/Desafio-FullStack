# Projeto de Cadastro de Desenvolvedores 🚀

Este projeto consiste em uma aplicação para cadastro de desenvolvedores associados a diferentes níveis. A aplicação é composta por um backend que oferece uma API RESTful e um frontend que é uma SPA (Single Page Application) interligada à API.

## Estrutura do Projeto 📂

- **backend**: Contém o código relacionado ao servidor e à API RESTful.
- **frontend**: Contém o código da interface do usuário.

## Dependências 📦

## Backend

Desenvolva uma API RESTful com os métodos GET, POST, PUT/PATCH e DELETE.

## Frontend

Crie uma SPA (Single Page Application) com uma interface intuitiva, aplicando técnicas de UI/UX.

## Configuração do Ambiente ⚙️

Certifique-se de ter as versões adequadas do Node.js e outras ferramentas necessárias instaladas em seu ambiente de desenvolvimento.

## Endpoints da API 🚚

- **Listar Níveis (GET):** `/api/niveis`
  - **Resposta de Sucesso (200):** Retorna a lista de níveis existentes.
  - **Resposta de Erro (404):** Retorna se não houver nenhum nível cadastrado.

- **Cadastrar Nível (POST):** `/api/niveis`
  - **Corpo da Requisição:** `{ "nivel": "Nome do Nível" }`
  - **Resposta de Sucesso (201):** Retorna o novo nível criado.
  - **Resposta de Erro (400):** Retorna se o corpo da requisição estiver incorreto.

- **Editar Nível (PUT/PATCH):** `/api/niveis/:id`
  - **Corpo da Requisição:** `{ "nivel": "Novo Nome do Nível" }`
  - **Resposta de Sucesso (200):** Retorna o nível editado.
  - **Resposta de Erro (400):** Retorna se o corpo da requisição estiver incorreto.

- **Remover Nível (DELETE):** `/api/niveis/:id`
  - **Resposta de Sucesso (204):** Retorna se o nível foi removido com sucesso.
  - **Resposta de Erro (400):** Retorna se houver desenvolvedores associados ao nível.

- **Listar Desenvolvedores (GET):** `/api/desenvolvedores`
  - **Resposta de Sucesso (200):** Retorna a lista de desenvolvedores existentes.
  - **Resposta de Erro (404):** Retorna se não houver nenhum desenvolvedor cadastrado.

- **Cadastrar Desenvolvedor (POST):** `/api/desenvolvedores`
  - **Corpo da Requisição:**

  ```json
  {
      "nivelId": 1,
      "nome": "Nome do Desenvolvedor",
      "sexo": "M",
      "datanascimento": "1990-01-01",
      "hobby": "Programação"
  }
   ```

  - **Resposta de Sucesso (201):** Retorna o novo desenvolvedor criado.
  - **Resposta de Erro (400):** Retorna se o corpo da requisição estiver incorreto.

- **Editar Desenvolvedor (PUT/PATCH):** `/api/desenvolvedores/:id`
  - **Corpo da Requisição:**

   ```json
   {
      "nome": "Novo Nome do Desenvolvedor",
      "hobby": "Violão",
      "nivelId": 2,
      "sexo": "F",
      "datanascimento": "1990-01-01"
  }
   ```

  - **Resposta de Sucesso (200):** Retorna o desenvolvedor editado.
  - **Resposta de Erro (400):** Retorna se o corpo da requisição estiver incorreto.

- **Remover Desenvolvedor (DELETE):** `/api/desenvolvedores/:id`
  - **Resposta de Sucesso (204):** Retorna se o desenvolvedor foi removido com sucesso.
  - **Resposta de Erro (400):** Retorna se houver problemas na remoção.

## Sugestões de Desenvolvimento

### Estrutura da base de desenvolvedores

```plaintext
id: integer
nivel: fk
nome: varchar
sexo: char
datanascimento: date
idade: integer
hobby: varchar
```

## Estrutura da base de níveis

```plaintext
id: integer
nivel: varchar
```

### Orquestração de Projetos

- Disponibilização do backend via Docker 🐳
- Disponibilização do frontend via Docker 🎨 🐳
- Disponibilização dos containers (backend + frontend) via Docker Compose 🐳
- Disponibilização/Publicação do sistema online 🌐

## Opcionais 📝

- Utilize tipagem de dados apropriada para garantir consistência nos dados.
- Mantenha um código limpo e bem estruturado, seguindo os princípios de Clean Code e Clean Architecture.
- Adicione testes unitários para partes críticas do código.
- Considere adicionar capturas de tela ou GIFs animados para demonstrar visualmente a interface do usuário.

## O que será avaliado? 🔎

Em geral, tudo! Porém, nosso foco aqui é descobrir como você aplica conceitos básicos da programação no seu dia a dia para solucionar e resolver problemas e principalmente, entregar valor ao produto!

Os mais importante aqui são:

- Sua lógica de programação
- Sua estrutura do código
- Sua metodologia aplicada
- Como você resolveu os problemas
- Sua forma de escrever o código

## Entrega 📄

Faça seu teste com calma! Organize-se! E após finalizado envie-nos por e-mail o link do projeto no github, com as devidas explicações no **README.md** do seu projeto.

Desejamos uma boa sorte e agradecemos o interesse em participar de nosso processo de obtenção de talentos!
