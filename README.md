Symfony Demo Application with docker
========================

The "Symfony Demo Application" is a reference application created to show how
to develop applications following the [Symfony Best Practices][1].

Requirements
------------

  * PHP 7.2.9 or higher;
  * composer 1.6.3 or higher;
  * docker 18.09 or higher;
  * docker-compose 1.17 or higher;

Version usage
-----
  * PHP 7.2.9;
  * Symfony 5.0;
  * Postgres 10.9;

Usage
-----

```bash
$ docker-compose up
```
In docker container execute:

```bash
php bin/console doctrine:migrations:diff
php bin/console doctrine:migrations:migrate
php bin/console doctrine:fixtures:load --purge-with-truncate
```