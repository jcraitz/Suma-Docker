FROM php:8.1-apache

RUN a2enmod rewrite

RUN apt-get update -y && apt-get install -y git unzip zip nano jq

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

WORKDIR /var/www/html

RUN chmod +x /usr/local/bin/install-php-extensions && \
    install-php-extensions zip gd bcmath pdo_mysql mcrypt xdebug @composer

WORKDIR /tmp
RUN curl -sL https://deb.nodesource.com/setup_14.x -o nodesource_setup.sh
RUN bash nodesource_setup.sh
RUN apt-get install nodejs
RUN rm nodesource_setup.sh
WORKDIR /var/www/html
COPY docker-config/index.html ./

# grunt stuff if we want to continue using it
# RUN npm install -g grunt-cli
# RUN npm install -g bower
# RUN npm update -g
# cd ./suma/analysis/
# npm install --no-bin-link
# grunt prepareDevEnv --force
