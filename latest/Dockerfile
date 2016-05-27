FROM tutum/lamp:latest

MAINTAINER Gildásio Júnior (gjuniioor@protonmail.com)

# Install DVWA
RUN \
	rm -rf /app/* && \
	apt-get update && \
	apt-get install -y wget && \
	rm -rf /var/lib/apt/lists/* && \
	wget https://github.com/RandomStorm/DVWA/archive/v1.9.tar.gz -O dvwa.tar.gz && \
	tar -xf dvwa.tar.gz && \
	cp -r DVWA-master/* /app/ && \
	rm -rf DVWA-master && \
	rm -rf dvwa.tar.gz

# Configure the db access
RUN \
	sed -i 's/root/admin/g' /app/config/config.inc.php && \
	echo "sed -i \"s/p@ssw0rd/\$PASS/g\" /app/config/config.inc.php" >> /create_mysql_admin_user.sh

EXPOSE 80 3306
CMD ["/run.sh"]
