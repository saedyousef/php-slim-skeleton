<h1 align="center">Slim Framework skeleton</h1>

<p align="center">
	<img src="https://github.com/robiningelbrecht/slim-skeleton-ddd-amqp/raw/master/readme/slim.webp" alt="Slim">
</p>

<p align="center">
<a href="https://github.com/robiningelbrecht/slim-skeleton-ddd-amqp/actions/workflows/ci.yml"><img src="https://github.com/robiningelbrecht/slim-skeleton-ddd-amqp/actions/workflows/ci.yml/badge.svg" alt="CI"></a>
<a href="https://codecov.io/gh/robiningelbrecht/slim-skeleton-ddd-amqp" ><img src="https://codecov.io/gh/robiningelbrecht/slim-skeleton-ddd-amqp/branch/master/graph/badge.svg?token=hgnlFWvWvw" alt="Codecov.io"/></a>
<a href="https://github.com/robiningelbrecht/slim-skeleton-ddd-amqp/blob/master/LICENSE"><img src="https://img.shields.io/github/license/robiningelbrecht/slim-skeleton-ddd-amqp?color=428f7e&logo=open%20source%20initiative&logoColor=white" alt="License"></a>
<a href="https://phpstan.org/"><img src="https://img.shields.io/badge/PHPStan-level%208-succes.svg?logo=php&logoColor=white&color=31C652" alt="PHPStan Enabled"></a>
<a href="https://php.net/"><img src="https://img.shields.io/packagist/php-v/robiningelbrecht/slim-skeleton-ddd-amqp/dev-master?color=%23777bb3&logo=php&logoColor=white" alt="PHP"></a>
</p>

---

This repository is a simple example on how to use <a href="https://github.com/slimphp/Slim">Slim Framework</a> and <a href="https://github.com/PHP-DI/PHP-DI">PHP-DI</a>

To Run on your local machine:

* Run `composer create-project --stability dev robiningelbrecht/slim-skeleton-ddd-amqp directory-name`
* Copy `.env.dist` to `.env`
* Run `docker-composer up -d --build` to up and build Docker containers
* Run `docker-compose run --rm php-cli composer install` to install dependencies
* Run `docker-compose run --rm php-cli vendor/bin/doctrine-migrations migrate` to bring db schema up to date.
* Run `docker-compose run --rm php-cli bin/console pokemon:cache` to store Pokemon in database.
* Run `docker-compose run --rm php-cli bin/console amqp:consume add-vote-command-queue` to start consuming vote queue
* Navigate to `http://localhost:8080` 
* Run test suite `docker-compose run --rm php-cli vendor/bin/phpunit`

@TODO: composer create-project with or without examples
@TODO: Add authentication

<h2 align="center">Voting example</h2>
<p align="center">
  <img src="https://github.com/robiningelbrecht/the-coolest-pokemon/raw/master/readme/vote.webp" alt="Vote">
</p>

<h2 align="center">Results example</h2>
<p align="center">
  <img src="https://github.com/robiningelbrecht/the-coolest-pokemon/raw/master/readme/results.webp" alt="Results">
</p>
