# Desafio-FullStack
Este é o escopo do projeto base para o teste de avaliação para o ingresso de novos desenvolvedores junto a **Gazin**\<Tech>

Esse desafio é composto de algumas etapas. O intuito não é de forma alguma que se tenha que implementa-lo completamente para qualquer consideração de contratação.

O projeto consiste em uma aplicação onde o candidato deverá desenvolver uma aplicação na *linguagem que desejar*, criando um Backend e um Frontend  que deverão estar interligados através de uma API REST JSON.
  
O propósito do teste é analisar boas práticas, lógica de programação, reaproveitamento de código e conhecimento geral das tecnologias escolhidas e utilizadas.

*Dica 1*: Fique tranquilo e tente resolvê-lo como se estivesse estudando algo novo que queira aprender.
*Dica 2*: Capriche no README do seu projeto! Seja especifico e aponte o que você julgar importante que nós saibamos para conseguir executa-lo de forma correta.

Crie um repositório público em algum serviço de hospedagem como GitHub, GitLab, BitBucket, para armazenar seu código. Você o enviará para nós, para a avaliação do código.

O objetivo desse desafio é compreender quais conhecimentos você já possui e sua desenvoltura diante a problemas ou tarefas que esteja se deparando pela primeira vez. Imagine que o resultado do seu trabalho será um projeto público que será utilizado por várias pessoas. Sendo assim, aplique neste projeto as boas práticas de desenvolvimento de software que você conhece.

## O Backend
Você deverá desenvolver uma API RESTful que utilize os métodos (​GET​, ​POST​, ​PUT/PATCH​ e ​DELETE​).

## O Frontend
Você deverá desenvolver uma interface da forma que achar melhor, aplicando técnicas de UI/UX a seu critério. Porém, esta interface deverá ser uma SPA (Single Page Application) e atender o consumo de todos endpoints da API do backend.

## Itens a serem entregues no projeto
* Os itens marcados com a tag [1] são os itens que cobrem o __mínimo viável do teste para que possamos avaliar o desempenho do candidato__;
* Os itens marcados com a tag [2] __são itens opcionais__, mas que poderão demonstrar o nível de conhecimento do candidato sobre a stack escolhida para realizar o teste;
* Os itens marcados com a tag [3] __são itens opcionais__, mas que poderão demonstrar o nível de conhecimento do candidato sobre a estruturação do projeto;
* Os itens marcados com a tag [4] __são itens opcionais__, mas que poderão demonstrar o nível de conhecimento do candidato sobre a construção do projeto (orquestração da aplicação);

## O projeto
O projeto consiste em criar um sistema de cadastro de Desenvolvedores, que deverá obrigatóriamente, estar associado a um determinado nível. 

O candidato deverá criar então **2 CRUDs completos**, sendo:

* CRUD de níveis
* CRUD dos desenvolvedores

Ambos os CRUDs deverão possuir todos os métodos REST citados no item [O backend](https://github.com/dmsysop/gazin-potencial-crud/blob/main/README.md#o-backend)

1. Os itens a serem desenvolvidos nesta etapa do projeto são para avaliação de domínio de stack escolhida:

TAG | STATUS CODE | ITEM
--- | ----------- | ------------
[1] | 200 | Listar níveis existentes
[1] | 201 ou 400 | Cadastrar um nível
[1] | 200 ou 400 | Editar um nível
[1] | 204 ou 400 | Remover um nível
[1] | 200 | Listar desenvolvedores existentes
[1] | 201 ou 400 | Cadastrar um desenvolvedor
[1] | 200 ou 400 | Editar um desenvolvedor
[1] | 204 ou 400 | Remover um desenvolvedor
[2] | 501 | Impedir que um nível seja removido quando houver um (ou mais) desenvolvedor(es) associado a este
[2] | 200 ou 404 | Adicionar funcionalidade de busca via query string para a listagem de níveis
[2] | 200 ou 404 | Adicionar funcionalidade de busca via query string para a listagem de desenvolvedores
[2] | - | Adicionar paginação na listagem de níveis
[2] | - | Adicionar paginação na listagem de desenvolvedores
[2] | - | Adicionar retorno visual às mensagens de sucesso e/ou erros (Toast Notification)
[2] | - | Adicionar retorno visual para confirmação da remoção dos itens do crud
[2] | - | Permitir a ordenação dos campos, selecionando o "título" (via thead) da tabela de listagem em forma crescente/decrescente
[2] | - | Validações de campos dos formulários
[2] | - | Exibir na listagem de níveis a quantidade de desenvolvedores associados a ele (nível) numa nova coluna


2. Os itens a serem desenvolvidos nesta etapa do projeto são para avaliação de conhecimento técnico e estruturação e organização de código:
> Lembramos que os itens abaixo são __opcionais__

TAG | ITEM
--- | ------------
[3] |  Tipagem de dados
[3] |  Organização e estrutura de pastas
[3] |  Conceitos e boas práticas de programação
[3] |  Reaproveitamento de código
[3] |  Clean Code
[3] |  Clean Architecture
[3] |  Testes Unitários
[3] |  Documentação de código/endpoint


3. Os itens a serem desenvolvidos nesta etapa do projeto são para avaliação de conhecimento técnico e orquestração de projetos:
> Lembramos que os itens abaixo são __opcionais__

TAG | ITEM
--- | ------------
[4] | Disponibilização do backend via Docker
[4] | Disponibilização do frontend via Docker
[4] | Disponibilização dos containers (backend+frontend) via Docker Compose
[4] | Disponibilização/Publicação do sistema em uma aplicação online (Ex. Heroku)


## Sugestões de Desenvolvimento

#### Estrutura da base de desenvolvedores:
```
id: integer
nivel: fk
nome: varchar
sexo: char
datanascimento: date
idade: integer
hobby: varchar
```

#### Estrutura da base de níveis:
```
id: integer
nivel: varchar
```

# O que será avaliado?
Em geral, tudo! Porém, nosso foco aqui é descobrir como você aplica conceitos básicos da programação no seu dia a dia para solucionar e resolver problemas e principalmente, entregar valor ao produto!

Os mais importante aqui são:

- Sua lógica de programação
- Sua estrutura do código
- Sua metodologia aplicada
- Como você resolveu os problemas
- Sua forma de escrever o código


# Entrega
Faça seu teste com calma! Organize-se! E após finalizado envie-nos por e-mail o link do projeto no github, com as devidas explicações no README do seu projeto.

Desejamos uma boa sorte e agradecemos o interesse em participar de nosso processo de obtenção de talentos!
