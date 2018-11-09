FROM php:7.0-cli-alpine

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer 

RUN apk add zip

RUN apk add py-pip && \
    pip install --upgrade pip

RUN pip install awscli && \
    pip install dump-env

CMD ["/bin/sh"]
