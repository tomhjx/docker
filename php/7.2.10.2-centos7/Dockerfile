FROM tomhjx/php:7.2.10-centos7
RUN /usr/local/php/bin/pecl install redis;
RUN /usr/local/php/bin/pecl install mongodb;

COPY etc/php.ini /usr/local/php/lib/php.ini
CMD ["php", "-v"]
