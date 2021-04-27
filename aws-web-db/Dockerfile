FROM amazonlinux

RUN yum -y update && \
    yum -y install httpd php mysql php-mysql wget tar.x86_64

WORKDIR /var/www/html

RUN wget https://s3-us-west-2.amazonaws.com/us-west-2-aws-training/awsu-spl/spl-13/scripts/app.tgz

RUN tar xvfz app.tgz

RUN chown apache:root /var/www/html/rds.conf.php

#web server
CMD apachctl -D FOREGROUND