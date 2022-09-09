FROM mysql:8.0

# ポートの解放
EXPOSE 3306

# settings
COPY ./my.cnf /etc/my.cnf

# timezone
RUN cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime

RUN mkdir /var/log/mysql && \
	chown mysql:mysql /var/log/mysql

# コマンド実行
CMD ["mysqld"]
