# Suma-Docker
Docker development version of the [Suma Project](https://github.com/suma-project)

## Installation
 - Install Docker (podman may work, but has not been tested, YMMV)
 - Clone or Download this repository.
 - From the project directory run:
   `cp .env.sample .env`
 - Using your favorite text editor or IDE modify any of the default environment variables to suit your needs.
 - Note: at least temporarily, you will need to manually edit the config files in docker-config in addition to the .env file
 - From a terminal application, type 
   `docker compose up --build -d`
 - Visit [http://localhost:8181](http://localhost:8181) in your web browser for a basic list of app endpoints.
 - Visit [http://localhost:8182](http://localhost:8182) in your web browser for a PHPMyAdmin interface to inspect the DB.
 - To shut down the containers and remove them, run
   `docker compose down`
 - If you don't need to rebuild, you can load up new containers with
   `docker compose up -d`

## Admin Tools
The Suma admin tools can be found at http://localhost:19679/sumaserver/admin. The default admin username is "admin" and admin password is "admin".

## Notes on using Docker

### Structure
#### High Level
#### app (server & client)
#### db
#### db-admin-app
#### network
### Managing / Starting / Stopping / Starting-Over

## PHP Version
Suma-Docker installs Suma in a PHP 8.x environment.

## Development 
To use Suma-Docker as a development environment for the Suma Client, you will need to use npm commands in the suma/web-sourcecode directory.

## NOTICE
This project is **not intended** for production use at this time. Please use this _only_ for testing or development deployments.
