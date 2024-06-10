# Projeto de Cadastro de Desenvolvedores 🚀

Este projeto consiste em uma aplicação para cadastro de desenvolvedores associados a diferentes níveis. A aplicação é composta por um backend que oferece uma API RESTful e um frontend que é uma SPA (Single Page Application) interligada à API.

## Estrutura do Projeto 📂

Sugerimos a seguinte estrutura de pasta inicial para o projeto:

```
- 📂sua-pasta
  - 📂backend
    - 🐳 Dockerfile
  - 📂frontend
    - 🐳 Dockerfile
  🐳 docker-compose.yml
```

### **Legenda:**

- 📂**sua-pasta**: Pasta raiz do projeto.
- 📂**backend**: Contém o código relacionado ao servidor e à API RESTful.
- 📂**frontend**: Contém o código da interface do usuário.
- 🐳**docker-compose.yml**: Arquivo de configuração do Docker Compose para orquestração dos containers.

> ⚠️ **Obs:** Crie apenas um único repositório que contenha front + backend.

## Banco de dados 📦

### Estrutura da base de desenvolvedores

```
id: integer
nivel_id: fk (niveis)
nome: varchar
sexo: char
data_nascimento: date
hobby: varchar
```

### Estrutura da base de níveis

```
id: integer
nivel: varchar
```

# **Backend** 🚀

Desenvolva uma API RESTful com os métodos GET, POST, PUT/PATCH e DELETE.

## Endpoints da API 🚚

Abaixo está como esperamos que sejam os endpoints da api.

> ⚠️ **Obs:** Fique atento aos requisitos adicionais ao final do documento.

### **Níveis**

- **Listar Níveis (GET):** `/api/niveis`

  - **Resposta de Sucesso (200):** Retorna a lista de níveis existentes.

  ```json
  {
    "id": 1,
    "nivel": "Nome do Nível"
  }
  ```

  - **Resposta de Erro (404):** Retorna se não houver nenhum nível cadastrado.

- **Cadastrar Nível (POST):** `/api/niveis`

  - **Corpo da Requisição:**

  ```json
  {
    "nivel": "Nome do Nível"
  }
  ```

  - **Resposta de Sucesso (201):** Retorna o novo nível criado.
  - **Resposta de Erro (400):** Retorna se o corpo da requisição estiver incorreto.

- **Editar Nível (PUT/PATCH):** `/api/niveis/:id`

  - **Corpo da Requisição:**

  ```json
  {
    "nivel": "Nome do Nível"
  }
  ```

  - **Resposta de Sucesso (200):** Retorna o nível editado.
  - **Resposta de Erro (400):** Retorna se o corpo da requisição estiver incorreto.

- **Remover Nível (DELETE):** `/api/niveis/:id`
  - **Resposta de Sucesso (204):** Retorna se o nível foi removido com sucesso.
  - **Resposta de Erro (400):** Retorna se houver desenvolvedores associados ao nível.

### **Desenvolvedores**

- **Listar Desenvolvedores (GET):** `/api/desenvolvedores`

  - **Resposta de Sucesso (200):** Retorna a lista de desenvolvedores existentes.

  ```json
  {
    "id": 1,
    "nome": "Nome do Desenvolvedor",
    "sexo": "M",
    "data_nascimento": "1990-01-01",
    "idade": 31,
    "hobby": "Programação",
    "nivel": {
      "id": 1,
      "nivel": "Nome do Nível"
    }
  }
  ```

  - **Resposta de Erro (404):** Retorna se não houver nenhum desenvolvedor cadastrado.

- **Cadastrar Desenvolvedor (POST):** `/api/desenvolvedores`

  - **Corpo da Requisição:**

  ```json
  {
    "nivel_id": 1,
    "nome": "Nome do Desenvolvedor",
    "sexo": "M",
    "data_nascimento": "1990-01-01",
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
    "nivel_id": 2,
    "sexo": "F",
    "data_nascimento": "1990-01-01"
  }
  ```

  - **Resposta de Sucesso (200):** Retorna o desenvolvedor editado.
  - **Resposta de Erro (400):** Retorna se o corpo da requisição estiver incorreto.

- **Remover Desenvolvedor (DELETE):** `/api/desenvolvedores/:id`
  - **Resposta de Sucesso (204):** Retorna se o desenvolvedor foi removido com sucesso.
  - **Resposta de Erro (400):** Retorna se houver problemas na remoção.

#### Observações

Caso faça paginação, retornar o seguinte formato de resposta:

```json
{
  "data": [], // Array de desenvolvedores ou níveis
  "meta": {
    "total": 10,
    "per_page": 10,
    "current_page": 1,
    "last_page": 1
  }
}
```

# **Frontend** 🎨

Crie uma SPA (Single Page Application) com uma interface intuitiva, aplicando técnicas de UI/UX.

Deverá ter pelo menos 2 páginas:

- Níveis
- Desenvolvedores

Para cada página:

- Listagem
  - Tabela com os itens cadastrados
  - Deve ter as opções de adicionar, editar e remover
- Cadastro / Edição
  - Pode ser uma modal ou uma página a parte também
- Exclusão
  - Deve ter uma confirmação antes de excluir

## O que será avaliado? 🔎

Em geral, tudo! Porém, nosso foco aqui é descobrir como você aplica conceitos básicos da programação no seu dia a dia para solucionar e resolver problemas e principalmente, entregar valor ao produto!

Os mais importante aqui são:

- Sua lógica de programação
- Sua estrutura do código
- Sua metodologia aplicada
- Como você resolveu os problemas
- Sua forma de escrever o código

## Dicas

- **Não se preocupe em fazer tudo de uma vez!**
  - Faça um passo de cada vez, resolvendo um problema de cada vez.
- **Em caso de dúvidas, pergunte!**
  - Estamos aqui para ajudar, caso fique com dúvida em alguns dos requisitos.
- **Utilize o que quiser**.
  - Seja frameworks, bibliotecas, banco de dados, etc...
- **Foque no que foi pedido**.
  - Não gaste tempo com funcionalidades que não foram solicitadas.
- **Cheque tudo!**
  - Certifique-se de que tudo está funcionando corretamente.
  - Antes de enviar, verifique se o projeto está funcionando corretamente.
    - Instale tudo do zero e teste novamente.
- **Não se esqueça de documentar o seu projeto!**
  - Explique como rodar o projeto, como testar, como foi a sua abordagem, etc...
  - Caso não utilize Docker, deixe as instruções de instalação e execução no **README.md**:
    - Versões utilizadas, scripts de banco dedos, passo a passo, etc...

## Entrega 📄

Faça seu teste com calma! Organize-se! E após finalizado envie-nos por e-mail o link do projeto no github, com as devidas explicações no **README.md** do seu projeto.

Desejamos uma boa sorte e agradecemos o interesse em participar de nosso processo de obtenção de talentos!

## Checklist 📝

Abaixo está todos os itens que iremos avaliar no seu projeto.
<br>
Quanto mais itens você conseguir entregar, melhor será a sua avaliação.
<br>
Este checklist é apenas um guia para te ajudar e não precisa ser seguido à risca.
Faça os itens que conseguir.
<br>
Está separado por níveis, onde o nível 1 é o mínimo que esperamos que você entregue.

---

**Legenda de Símbolos:**

- 🚀 -> Backend
- 🎨 -> Frontend

> **⚠️ Obs:** Quando tiver ambos os simbolos, deve-se fazer a feature no frontend e backend.

---

### Nível 1

|     | Descrição                  | Local |
| --- | -------------------------- | ----- |
| [ ] | Listar niveis              | 🚀🎨  |
| [ ] | Cadastrar um nível         | 🚀🎨  |
| [ ] | Editar um nível            | 🚀🎨  |
| [ ] | Remover um nível           | 🚀🎨  |
| [ ] | Listar desenvolvedores     | 🚀🎨  |
| [ ] | Cadastrar um desenvolvedor | 🚀🎨  |
| [ ] | Editar um desenvolvedor    | 🚀🎨  |
| [ ] | Remover um desenvolvedor   | 🚀🎨  |

### Nível 2

|     | Descrição                                                              | Local |
| --- | ---------------------------------------------------------------------- | ----- |
| [ ] | Impedir remoção de nível com desenvolvedores associados                | 🚀    |
| [ ] | Adicionar busca via query para a listagem de n íveis                   | 🚀🎨  |
| [ ] | Adicionar busca via query para a listagem de desenvolvedores           | 🚀🎨  |
| [ ] | Tratamento de Exceções / Retornos erros concisos                       | 🚀🎨  |
| [ ] | Paginação na listagem de níveis                                        | 🚀🎨  |
| [ ] | Paginação na listagem de desenvolvedores                               | 🚀🎨  |
| [ ] | Mensagens de sucesso e/ou erros (Ex. Toast Notification)               | 🎨    |
| [ ] | Confirmação para exclusão de itens                                     | 🎨    |
| [ ] | Ordenação das tabelas clicando no nome da coluna                       | 🎨    |
| [ ] | Validações de campos                                                   | 🚀🎨  |
| [ ] | Na página de níveis adicionar uma coluna com a qtde de devs associados | 🎨    |

### Nível 3

|     | Descrição                              | Local |
| --- | -------------------------------------- | ----- |
| [ ] | Tipagem de dados                       | 🚀🎨  |
| [ ] | Organização e estrutura de pastas      | 🚀🎨  |
| [ ] | Reaproveitamento de código             | 🚀🎨  |
| [ ] | Clean Code                             | 🚀🎨  |
| [ ] | Arquitetura: Clean, Onion, Hexagonal   | 🚀🎨  |
| [ ] | Testes unitários / Feature             | 🚀🎨  |
| [ ] | Documentação código/endpoint (swagger) | 🚀🎨  |

### Nível 4

|     | Descrição                                                               | Local |
| --- | ----------------------------------------------------------------------- | ----- |
| [ ] | Disponibilização do backend via Docker                                  | 🚀    |
| [ ] | Disponibilização do frontend via Docker                                 | 🎨    |
| [ ] | Disponibilização dos containers (backend + frontend) via Docker Compose | 🚀🎨  |
| [ ] | Publicação do projeto online                                            | 🚀🎨  |
