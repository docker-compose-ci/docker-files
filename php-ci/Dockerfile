FROM php:5.6

RUN apt-get update && \
pecl install mongodb && \
pecl install redis && \
echo "extension=mongodb.so" >> /usr/local/etc/php/conf.d/ext.ini  && \
echo "extension=redis.so" >> /usr/local/etc/php/conf.d/ext.ini  && \
