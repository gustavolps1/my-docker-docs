# MYSQL NODEJS COM DOCKER E DOCKER COMPOSE NO UBUNTU 18.04

## Links

> MySQL Container: https://hub.docker.com/_/mysql

> Ultima versão Docker Compose: https://docs.docker.com/compose/install/

> Versões Docker Compose:  https://github.com/docker/compose/releases


## Instalando Docker

#### Certifique-se do apt estar atualizado

```sh 
sudo apt update
```

#### Download e instação via apt

```sh 
sudo apt install docker.io ```
```
#### Testando a instalação do docker

```sh 
docker --version 
```

## Instalando Docker Compose

#### Certifique-se do apt estar atualizado

```sh 
sudo apt update
```
#### Instalando o curl via apt

```sh
-sudo apt install curl
```
#### Download e instalação do Docker Compose 1.25.3
```sh   
sudo curl -L "https://github.com/docker/compose/releases/download/1.25.3/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose 
```
