FROM debian:buster-slim

RUN apt-get update && apt-get install -y mariadb-server && rm -rf /var/lib/apt/lists/*

COPY my.cnf /etc/mysql/my.cnf

# Add this line to change the ownership of the data directory
RUN chown -R mysql:mysql /var/lib/mysql

EXPOSE 3306

CMD ["mysqld_safe"]