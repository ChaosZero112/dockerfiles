FROM mariadb:10.7
LABEL org.label-schema.schema-version="1.0.0-rc1"
LABEL org.label-schema.vendor="EasyEngine"
LABEL org.label-schema.name="db"

RUN rm /etc/mysql/my.cnf && rm /etc/mysql/mariadb.cnf && rm -rf /etc/mysql/mariadb.conf.d
COPY ee.cnf  /etc/mysql/conf.d/ee.cnf
COPY my.cnf  /etc/mysql/
