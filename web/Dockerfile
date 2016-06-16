FROM ubuntu:14.04
MAINTAINER Javier Núñez Berrocoso <javiernuber@gmail.com>

RUN apt-get update && \
    apt-get -y install apache2 php5 libapache2-mod-php5 php5-mcrypt php5-json php5-gd curl git && \
    apt-get clean && \
    update-rc.d apache2 defaults && \
    php5enmod mcrypt && \
    rm -rf /var/www/html && \
    curl -sS https://getcomposer.org/installer | php && \
    mv composer.phar /usr/local/bin/composer

EXPOSE 80
EXPOSE 443

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]