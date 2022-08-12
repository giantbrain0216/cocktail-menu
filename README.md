# Cocktail Menu
An interactive menu where you can choose and order your favourite drinks 🍺🍹

# Summary
1. [Demo](#demo)
2. [Prerequisites](#prerequisites)
3. [Stack](#stack)
4. [Getting started](#getting-started)
5. [Useful commands](#useful-commands)
6. [Credits](#credits)

# Demo

![Demo](https://raw.githubusercontent.com/lgcolella/cocktail-menu/master/.repository/demo.gif "Demo")

# Prerequisites

- Docker Compose >= 3.3

# Stack

![Laravel](https://raw.githubusercontent.com/lgcolella/cocktail-menu/master/.repository/laravel.png "Laravel")
![React](https://raw.githubusercontent.com/lgcolella/cocktail-menu/master/.repository/react.png "React")
![Typescript](https://raw.githubusercontent.com/lgcolella/cocktail-menu/master/.repository/typescript.png "Typescript")
![Bootstrap](https://raw.githubusercontent.com/lgcolella/cocktail-menu/master/.repository/bootstrap.png "Bootstrap")
![MySQL](https://raw.githubusercontent.com/lgcolella/cocktail-menu/master/.repository/mysql.png "MySQL")
![Nginx](https://raw.githubusercontent.com/lgcolella/cocktail-menu/master/.repository/nginx.png "Nginx")
![Docker](https://raw.githubusercontent.com/lgcolella/cocktail-menu/master/.repository/docker.png "Docker")


# Navigate into the project folder
cd cocktail-menu

# Generate the .env from the default one
cp .env.example .env

# Start docker-compose with services
docker-compose up -d

# Setup Laravel and install dependencies
docker-compose exec app bash -c "./scripts/install.sh"
```
> According to your env, you may need to give executable permissions to `composer.phar` and `./scripts/install.sh` to execute the above commands. You may also need to give readable and writable permission to `/storage` folder to make the application working fine.

Then you can visit the application at `localhost:8000`.

> If you installed Docker by using Docker Toolbox, you may need to replace `localhost` with the output of `docker-machine ip`.

If you want manage the database with a visual GUI, you can use Adminer at `localhost:8080` (The database credentials are those in the .env file).

# Useful commands

```sh
# Start application and related services
docker-compose up -d

# Shut down application and services
docker-compose down

# Shut down application, services and delete volumes, orphans containers and images
docker-compose down -v --remove-orphans --rmi=all

# Log to the bash of the app container
docker-compose exec app bash
```

When you log into the app container, you can run any php or nodejs script. For example:

```sh
# Build the frontend assets
npm run prod

# Build the frontend assets on change
npm run watch

# Prettify the code
npm run prettify

# Update the Composer autoloader
composer dump-autoload

# Run the Artisan Tinker shell
php artisan tinker
```
