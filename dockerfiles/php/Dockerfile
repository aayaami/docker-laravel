FROM php:8.1.2-fpm-alpine

RUN docker-php-ext-install pdo pdo_mysql

ARG UID
ARG GID

ENV UID=${UID}
ENV GID=${GID}

RUN addgroup -g ${GID} --system laravel
RUN adduser -G laravel --system -D -s /bin/sh -u ${UID} laravel

USER laravel