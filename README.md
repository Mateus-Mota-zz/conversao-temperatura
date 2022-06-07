# Projeto de Pipeline CI/CD para o build de uma aplicação de Conversão Temperatura

<br>

## Pré-requisitos

* Git
* Docker

<br>

## Ambiente testado

* git version 2.35.1
* Docker version 20.10.14

<br>

## Outras tecnologias utilizadas

* Github Actions
* Nginx

<br>

## Link da imagem no Docker registry

* https://hub.docker.com/repository/docker/mateusmotaa/conversao-temperatura

<br>

## Passo a Passo

### 1° Passo, realizar o fork do projeto oficial
Repositório oficial: https://github.com/KubeDev/conversao-temperatura

### 2° Passo, realizar o clone do projeto
~~~bash
git clone https://github.com/Mateus-Mota/conversao-temperatura
~~~

### 3° Passo, criação do dockerfile
* Definido a imagem base como Node devido a ser uma aplicação Node e escolhido uma versão mais recente e compatível com todos os requisitos do projeto.
* Criado diretório de trabalho no container e repassado apenas os arquivos que possuem as dependências para aplicação.
* Utilizado o NPM para instalar as dependências.
* Utilizado o EXPOSE 8080 para expor a porta do Container 
* Utilizado CMD para o comando node inicie a aplicação por via do parâmentro node.js


### 4° Passo, Utilização do Github Actions para pipeline CI-CD
* Criado os diretórios .github/workflows como requisitado na documentação e criado o arquivo main.yml
#### CI
* Criado os secrets DOCKERHUB_USER e DOCKERHUB_PWD no github para permitir o acesso ao dockerhub de forma segura
* Utilizado o variável github.run_number para saber numerar a versão e a atualizar a mais recente a cada push realizado
#### CD
*
*




