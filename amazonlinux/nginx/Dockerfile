FROM amazonlinux:latest

ENV TZ Asia/Tokyo

RUN amazon-linux-extras enable nginx1

RUN yum clean metadata && \
    yum update -y && \
    yum install -y nginx

COPY ./conf/nginx.conf /etc/nginx/nginx.conf
# COPY ./conf/php-default.conf /etc/nginx/conf.d/default.conf


ENTRYPOINT ["/usr/sbin/nginx", "-g", "daemon off;"]