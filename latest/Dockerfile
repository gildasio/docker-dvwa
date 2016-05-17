FROM debian:latest

MAINTAINER Gildásio Júnior (gjuniioor@protonmail.com)

# install apache
# install php
# install mysql
# install wget tar
# download https://github.com/RandomStorm/DVWA/archive/master.tar.gz
# https://github.com/RandomStorm/DVWA/archive/v1.9.tar.gz
# https://github.com/RandomStorm/DVWA/archive/v1.0.8.tar.gz
# install dvwa
# rm master.tar.gz
# rm -rf /var/cache/apk/*
#RUN	apk add --update apache2 mysql php-apache2 php-mysql php-gd
#RUN apk add --update apache2 php-apache2


RUN apt-get update && apt-get -y install apache2 mysql-server php5 php5-mysql php5-gd wget

RUN wget https://github.com/RandomStorm/DVWA/archive/v1.0.8.tar.gz -O dvwa.tar.gz
RUN tar -xf dvwa.tar.gz
RUN rm -rf /var/www/*
RUN cp -r DVWA-1.0.8/* /var/www/*
RUN rm -rf DVWA-1.0.8
RUN rm dvwa.tar.gz

RUN rm -rf /var/lib/apt/lists/*

# service apache2 restart

#RUN rm -rf /var/cache/apk/*

EXPOSE 80 3306

# run apache with php and mysql
CMD [""]
ENTRYPOINT [""]
