###################
# Como utitilizar #
###################

Clone o repositório usando o comando:
git clone https://github.com/danielnogueira-dev/Docker-Compose-Nginx-Php-Laravel-Mysql

Entre na pasta Docker-Compose-Nginx-Php-Laravel-Mysql e copie o arquivo env-example para .env.
cp env-example .env

Rode seu container:
docker-compose up -d

Adicione os domínios no arquivo de hosts do windows.
127.0.0.1 localhost

127.0.0.1 api.dev

Acessar o shell do container:
winpty docker exec -it nginx bash

winpty docker exec -it php-fpm bash

winpty docker exec -it mysql bash

Instruções iniciais para rodar o Laravel no localhost:

Entre em: winpty docker exec -it php-fpm bash
Acessar a pasta: cd /var/www/html

Executar comando para criar pasta vendor do laravel: composer install

Executar comando para criar arquivo de variáveis de ambiente do laravel: cp .env.example .env

Executar comando para gerar chaves necessarias para rodar o laravel: php artisan key:generate

Instruções iniciais para rodar o Laravel no api.dev:
Acessar a pasta api.dev: cd /var/www/html/api.dev

Executar comando para criar pasta vendor do laravel: composer install

Executar comando para criar arquivo de variáveis de ambiente do laravel: cp .env.example .env

Executar comando para gerar chaves necessarias para rodar o laravel: php artisan key:generate

Abra no navegador
http://localhost

http://api.dev

Acessar o banco de dados dentro do container Mysql
mysql -u root -p

Comandos básicos para utilizar o banco de dados
show databases;

CREATE DATABASE teste;

use teste;

show tables;