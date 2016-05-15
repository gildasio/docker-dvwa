FROM debian:jessie

MAINTAINER Gildásio Júnior (gjuniioor@protonmail.com)

RUN apt-get update && apt-get -y install apache2 mysql-server php5 php5-mysql php5-gd wget && rm -rf /var/lib/apt/lists/*
RUN wget https://github.com/RandomStorm/DVWA/archive/v1.0.8.tar.gz -O dvwa.tar.gz
RUN tar -xf dvwa.tar.gz
RUN rm -rf /var/www/* && cp -r DVWA-1.0.8/* /var/www/*
RUN rm -rf DVWA-1.0.8 && rm dvwa.tar.gz

EXPOSE 80 3306

CMD ["service", "apache2", "start"]
ENTRYPOINT [""]
