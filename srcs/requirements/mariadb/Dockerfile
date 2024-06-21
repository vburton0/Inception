FROM debian:bullseye

RUN apt-get update
RUN apt-get install -y \
    mariadb-server \
  && rm -rf /var/lib/apt/lists/* 

COPY conf/50-server.cnf /etc/mysql/mariadb.conf.d/50-server.cnf
COPY tools/entryPoint.sh /
RUN chmod +x /entryPoint.sh

ENTRYPOINT ["bash", "entryPoint.sh"]
