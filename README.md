# Processo Seletivo G4F

# Back End

## Descrição
Um sistema de controle de items de um achados e perdidos, implementado em Typescript Angular e Java Spring Boot, com banco de dados relacional MySQL.

## Configurações da máquina de desenvolvimento
* Ubuntu 18.04 64x
* JDK 11
* openjdk version "11.0.11" 2021-04-20
* Angular CLI: 12.2.10
* Node: 14.18.0
* npm 6.14.15

## Pré-Requisitos
* Ter todas as dependências citadas acima.
* Para executar o programa, é necessário que tanto o Frontend quando o [Front End](https://github.com/luisgaboardi/FindItems-Frontend) estejam rodando na mesma máquina.

### Criar banco de dados
Abra o terminal e o cliente do MySQL como um usuário capaz de criar outros usuários, por exemplo o root.

```$ sudo mysql -u root -p```

Crie uma nova base de dados:

```mysql> create database db_example;```

Crie o usuário e o dê os privilégios desse banco:

```mysql> create user 'springuser'@'%' identified by 'ThePassword';```

```mysql> grant all on db_example.* to 'springuser'@'%';```

### Linkar o banco de dados criado com a aplicação:

No arquivo **resources/application.properties**, substitua os valores de acordo com o nome que deu ao banco de dados e ao usuário:

```spring.datasource.url=jdbc:mysql://${MYSQL_HOST:localhost}:3306/db_example```

```spring.datasource.username=springuser```

```spring.datasource.password=ThePassword```

## Execução
Execute através de uma IDE.