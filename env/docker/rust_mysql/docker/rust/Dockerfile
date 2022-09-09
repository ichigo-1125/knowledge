FROM rust:latest

WORKDIR ./var/www/html/

RUN apt-get update -y && apt-get upgrade -y && \
	apt-get install -y mariadb-client
