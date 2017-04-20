FROM alpine:3.1

# Install modules
RUN apk update && apk add \
    make \
    gcc \
    g++ \
    autoconf \
    bison \
    curl-dev \
    libxml2-dev \
    openssl-dev \
    gd-dev \
    libvpx-dev

RUN cd /tmp/ \
    && curl -L https://github.com/sgolemon/php-src/archive/pipe.operator.tar.gz > pipe.operator.tar.gz \
    && tar xzf pipe.operator.tar.gz \
    && cd php-src-pipe.operator \
    && ./buildconf --force \
    && ./configure \
        --prefix=/usr/local/php \
        --enable-mbstring \
        --with-curl \
        --with-openssl \
        --with-xmlrpc \
        --enable-soap \
        --enable-zip \
        --with-mysql \
        --enable-embedded-mysqli \
    && make \
    && make install

CMD ["php"]
