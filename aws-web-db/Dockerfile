FROM amazonlinux

RUN yum -y update && \
    yum -y install httpd php mysql php-mysql wget tar.x86_64

WORKDIR /var/www/html

RUN wget https://s3-us-west-2.amazonaws.com/us-west-2-aws-training/awsu-spl/spl-13/scripts/app.tgz

RUN tar xvfz app.tgz

RUN chown apache:root /var/www/html/rds.conf.php

#Restart web server
#amazon-linux-httpd [enable | disable]
RUN echo "apachctl restart" >> /root/run_webserver.sh && \
    echo "apachctl restart" >> /root/run_webserver.sh && \
    chmod 755 /root/run_webserver.sh

CMD /root/run_webserver.sh