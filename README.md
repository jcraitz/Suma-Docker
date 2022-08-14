# Suma-Docker
Docker development version of the [Suma Project](https://github.com/suma-project)

## Installation
 - Install Docker
 - Clone or Download this repository.
 - From the project directory run:
   `cp .env.sample .env`
 - Using your favorite text editor or IDE modify any of the default environment variables to suit your needs.
 - From a terminal application, type 
   `docker-compose up -d`
 - Visit [http://localhost:8181](http://localhost:8181) in your web browser for a basic list of app endpoints.
 - Visit [http://localhost:8182](http://localhost:8182) in your web browser for a PHPMyAdmin interface to inspect the DB.

## Admin Tools
The Suma admin tools can be found at http://localhost:19679/sumaserver/admin. The default admin username is "sumaadmin" and admin password is "sumaadmin".

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
