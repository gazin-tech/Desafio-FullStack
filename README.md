# Desafio-FullStack
Esse desafio é composto de algumas etapas. O intuito não é de forma alguma que se tenha que implementa-lo completamente para qualquer consideração de contratação.

*Dica 1*: Fique tranquilo e tente resolvê-lo como se estivesse estudando algo novo que queira aprender.
*Dica 2*: Capriche no README do seu projeto! Seja especifico e aponte o que você julgar importante que nós saibamos para conseguir executa-lo de forma correta.

O objetivo desse desafio é compreender quais conhecimentos você já possui e sua desenvoltura diante a problemas ou tarefas que esteja se deparando pela primeira vez.

Imagine que o resultado do seu trabalho será um projeto público que será utilizado por várias pessoas. Sendo assim, aplique neste projeto as boas práticas de desenvolvimento de software que você conhece.

Crie um repositório público em algum serviço de hospedagem como GitHub, GitLab, BitBucket, para armazenar seu código. Você o enviará para nós, para a avaliação do código.

# Backend
Desenvolver uma API JSON REST na *linguagem a sua escolha*, que utilize os métodos (​GET​, ​POST​, ​PUT​, DELETE​).

# Frontend
UI/UX fica a critério do desenvolvedor porém deverá ser SPA (single-page application) e atender o consumo de todos endpoints da API.

# Especificação
Monte uma base de desenvolvedores com a seguinte estrutura:

```
nome: varchar
sexo: char
idade: integer
hobby: varchar
datanascimento: date
```

Utilize o ​banco de dados​ de sua preferência para armazenar os dados que a API irá consumir.

# API endpoints

```
GET /developers
Codes 200
```
Retorna todos os desenvolvedores

```
GET /developers?
Codes 200 / 404
```
Retorna os desenvolvedores de acordo com o termo passado via querystring e
paginação

```
GET /developers/{id}
Codes 200 / 404
```
Retorna os dados de um desenvolvedor

```
POST /developers
Codes 201 / 400
```
Adiciona um novo desenvolvedor

```
PUT /developers/{id}
Codes 200 / 400
```
Atualiza os dados de um desenvolvedor

```
DELETE /developers/{id}
Codes 204 / 400
```
Apaga o registro de um desenvolvedor


# Entrega
Desejável aplicação e o banco deve rodar em docker

# O que será avaliado
- Estrutura do código;
- Lógica de progamação;
- Clean Code;
- Clean Arch;
- Teste Unitários;
- Implementação de Docker para execução do ambiente;
- Controle de versão (GIT);
- Documentação do projeto;


Após finalizado enviar por e-mail o link do projeto no github, com explicação no README.
