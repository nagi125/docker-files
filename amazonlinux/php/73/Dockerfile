FROM amazonlinux:latest

ENV TZ Asia/Tokyo

RUN yum update -y && \ 
    amazon-linux-extras install php7.3 -y

COPY ./conf/php.ini /etc/php.ini
COPY ./conf/www.conf /etc/php-fpm.d/www.conf

EXPOSE 9000

ENTRYPOINT /usr/sbin/php-fpm -F