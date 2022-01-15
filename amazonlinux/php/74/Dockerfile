FROM amazonlinux:latest

ENV TZ Asia/Tokyo

RUN amazon-linux-extras enable php7.4

RUN yum clean metadata && \
    yum update -y && \
    yum install -y php-cli php-pdo php-fpm php-json php-mysqlnd \

# postgresqlを利用する場合
# php-pgsql

COPY ./conf/php.ini /etc/php.ini
COPY ./conf/www.conf /etc/php-fpm.d/www.conf

EXPOSE 9000

ENTRYPOINT ["/usr/sbin/php-fpm",  "-F"]
