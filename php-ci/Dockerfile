FROM php:5.6

RUN apt-get update -y && \
apt-get install pkg-config libssl-dev libzip-dev unzip -y && \
pecl install mongodb && \
pecl install redis && \
pecl install zip && \
echo "extension=mongodb.so" >> /usr/local/etc/php/conf.d/ext.ini  && \
echo "extension=zip.so" >> /usr/local/etc/php/conf.d/ext.ini  && \
echo "extension=redis.so" >> /usr/local/etc/php/conf.d/ext.ini && \
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" && \
php -r "if (hash_file('SHA384', 'composer-setup.php') === '669656bab3166a7aff8a7506b8cb2d1c292f042046c5a994c43155c0be6190fa0355160742ab2e1c88d40d5be660b410') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;" && \
php composer-setup.php --install-dir=bin --filename=composer && \
php -r "unlink('composer-setup.php');" && \
echo "export COMPOSER_ALLOW_SUPERUSER=1" >> ~/.bashrc

RUN php -r "copy('http://static.phpmd.org/php/2.6.0/phpmd.phar','/bin/phpmd');" && \
chmod 777 /bin/phpmd

RUN apt-get remove pkg-config libssl-dev unzip -y && \
apt-get autoremove --purge -y

CMD /bin/composer
