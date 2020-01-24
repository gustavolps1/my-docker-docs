## MYSQL COM DOCKER E DOCKER COMPOSE NO UBUNTU 18.04

> Tutorial referente as instalações das ferramentas Docker e Docker Compose utilizando o container MySQL

## 1. Instalando o Docker

Certifique-se do apt estar atualizado

```sh 
sudo apt update
```

Download e instação do docker via apt

```sh 
sudo apt install docker.io ```
```

Testando o comando docker

```sh 
sudo docker --version 
```

## 2. Instalando o Docker Compose

Certifique-se do apt estar atualizado

```sh 
sudo apt update
```
Instalando o curl via apt

```sh
-sudo apt install curl
```

Download e instalação do **Docker Compose 1.25.3**

```sh   
sudo curl -L "https://github.com/docker/compose/releases/download/1.25.3/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose 
```

Alterando permissões

```sh 
sudo chmod +x /usr/local/bin/docker-compose
```

Testando o docker-compose

```sh 
sudo docker-compose --version
```

## 3. Adicionando o usuário ubuntu ao grupo docker
Para utilização dos comandos docker sem a necessidade de iniciar a linha de comando com a keyword **sudo**

```sh 
sudo usermod -aG docker $USER
```

Agora é necessario estar relogando o usuário ubuntu

```sh 
su - $USER
```

Testando o comando docker

```sh 
docker ps
```
Pronto agora você não precisa mais ficar inserindo **sudo** na frente dos comandos **docker**

## 4. Instalando o container MySQL no Docker

> Nome do container:  nome-container

> Senha MySQL: 123123

> Porta MySQL: 3306

Copie e cole no terminal de comando

```sh 
docker run --name nome-container -e MYSQL_ROOT_PASSWORD=123123 -p 3306:3306 -d mysql
```
Pronto, agora você tem um container rodando o MySQL

```sh 
docker ps
```

Por algum motivo caso o container não seja rodando utilize

```sh 
docker ps -l
```
Ou

```sh
docker ps --filter "status=exited"
```
E veja o respectivo nome do container no campo **NAMES** e execute

```sh
docker start nome-container
``````
## 5. Conectando ao banco de dados MySQL via bash

Primeiramente certifique-se que seu container MySQL esteja rodando

```sh 
docker ps
```

Executando o container MySQL 

```sh 
docker exec -it nome-container bash 
```

Conectando com a base de dados

```sh 
mysql -uroot -p123123
```

Pronto agora se tudo deu certo você estará utilizando a bash do MySQL

```sh 
show databases;
```

## Links

>  Ultima versão Docker Compose: https://docs.docker.com/compose/install/

>  Versões Docker Compose:  https://github.com/docker/compose/releases

## Referências

> Node JS Mysql e Docker https://www.youtube.com/watch?v=frK8xb3kgeM

> Como Instalar o Docker e Docker Compose Ubuntu 18.04 https://www.youtube.com/watch?v=bpbcu36t7g0

> How To Create And Test MySQL Database Server in Docker On Ubuntu Linux https://www.youtube.com/watch?v=w_aVnMmrASE



