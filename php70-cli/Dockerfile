FROM php:7.0-cli-alpine

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer 

RUN apk add zip && apk add openssh && apk add rsync 

RUN apk add py-pip && \
    pip install --upgrade pip

RUN pip install awscli && \
    pip install dump-env

RUN apk add --no-cache libpng libpng-dev && docker-php-ext-install gd && apk del libpng-dev

CMD ["/bin/sh"]
