From mysql:latest
MAINTAINER Songjie Wang "wangso@missouri.edu"

ARG DEBIAN_FRONTEND=noninteractive
ENV MYSQL_ROOT_PASSWORD=root
ENV MYSQL_USER=covid19-user
ENV MYSQL_PASSWORD=covid19-pass
ENV MYSQL_DATABASE=covid19
RUN yum -y update && yum -y install net-tools && yum install nano
COPY covid19.sql /docker-entrypoint-initdb.d
ENTRYPOINT ["/entrypoint.sh"]
CMD ["mysqld"]

