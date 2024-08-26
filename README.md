# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

## Instruções gerais

Para executar o projeto é necessário ter instaladas as versões do Ruby e do Rails especificadas no Gemfile

```bash
bundle install
```

```bash
yarn install 
```

```bash
rails s -b 0.0.0.0 
```
o projeto será executado em modo de desenvolvimento

## Instruções para executar em produção

* primeiro apague o arquivo `credentials.yml.enc` e depois crie uma nova `master.key`  com o comando 

    ```bash 
        EDITOR=nano rails credentials:edit 
    ```

* Use o comando abaixo para pré compilar o projeto
    ```bash 
       RAILS_ENV=production rails assets:precompile 
    ```
* Use o comando abaixo para levantar um servidor em produção na sua máquina
    ```bash 
       RAILS_ENV=production rails s -b 0.0.0.0 
    ```  
* Em produção eu configurei o banco de dados Postgres, eu também configurei ele para rodar no Docker, use o comando abaixo para criar o banco de dados

    ```bash 
       docker compose up 
    ```  
* Use o comando abaixo para para migrar as tabelas    

    ```bash 
       RAILS_ENV=production rails db:migrate 
    ```  

* Eu também configurei um pgAdmin abra o arquivo `docker-compose.yml` para ver mais detalhes

    
