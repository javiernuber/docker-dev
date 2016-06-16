FROM mysql:5.6

MAINTAINER Javier Núñez Berrocoso <javiernuber@gmail.com>

RUN usermod -u 1000 mysql && \
		mkdir -p /var/run/mysqld && \
		chmod -R 777 /var/run/mysqld