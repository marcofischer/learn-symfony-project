FROM unit:1.30.0-php8.2

RUN apt-get update \
    && apt-get -y install zip libicu-dev zlib1g-dev libzip-dev libpq-dev curl \
    && cd /tmp && curl -1sLf 'https://dl.cloudsmith.io/public/symfony/stable/setup.deb.sh' | bash && apt install -y symfony-cli \
    && rm -rf /var/lib/apt/lists/* \
    && docker-php-ext-install pdo_mysql pdo_pgsql intl zip opcache

COPY --chown=unit:unit ./build/unit/config.json /docker-entrypoint.d
COPY --from=composer:2 /usr/bin/composer /usr/local/bin/composer

WORKDIR /app