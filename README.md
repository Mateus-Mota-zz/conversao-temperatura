# Projeto de Pipeline CI/CD para o build de uma aplicação de Conversão Temperatura

O passo a passo do projeto foi desenvolvido durante o evento Iniciativa Kubernetes

## Pré-requisitos

* Git
* Docker

## Passo a Passo

### 1° Realizando o clone desse projeto
~~~bash
git clone https://github.com/Mateus-Mota/conversao-temperatura.git
~~~

### 2° Criação de uma nova imagem.
~~~bash
docker build -t mateusmota/conversao-temperatura:v1 .
~~~

### 3° Criação da tag "latest"
~~~bash
docker tag mateusmota/conversao-temperatura:v1 mateusmota/conversao-temperatura:latest
~~~

### 4° Realização do push da sua imagem para o DockerHub.
~~~bash
docker push mateusmota/conversao-temperatura:v1
docker push mateusmota/conversao-temperatura:latest
~~~





