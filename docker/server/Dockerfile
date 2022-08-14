FROM php:8.1-apache

RUN a2enmod rewrite

RUN apt-get update && apt-get install -y git unzip zip

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

WORKDIR /var/www/html

RUN chmod +x /usr/local/bin/install-php-extensions && \
    install-php-extensions zip gd bcmath pdo_mysql mcrypt xdebug @composer

COPY docker-config/index.html /var/www/html/

WORKDIR /tmp
RUN curl -sL https://deb.nodesource.com/setup_14.x -o nodesource_setup.sh
RUN bash nodesource_setup.sh
RUN apt-get install nodejs
RUN rm nodesource_setup.sh
WORKDIR /var/www/html

RUN npm install -g grunt-cli
RUN npm install -g bower
RUN npm update -g

# cd ./suma/analysis/
# npm install --no-bin-link
# grunt prepareDevEnv --force
# RUN mkdir /var/www/app
# WORKDIR /var/www/app/
# COPY --from=builder /docker-config/analysis/config/config.yaml /var/www/app/suma/analysis/config/config.yaml
# COPY --from=builder /docker-config/service/config/config.yaml /var/www/app/suma/service/config/config.yaml
# COPY --from=builder /docker-config/service/web/config/config.yaml /var/www/app/suma/service/web/config/config.yaml
# COPY --from=builder /docker-config/web/config/spaceassessConfig.js /var/www/app/suma/web/config/spaceassessConfig.js

# ARG analysis_config=docker-config/analysis/config.yml
# ENV ANALYSIS_CONFIG ${analysis_config}

# COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/
# RUN install-php-extensions devel gd mcrypt bcmath zip xdebug @composer

# COPY --from=composer:2.0 /usr/bin/composer /usr/local/bin/composer
