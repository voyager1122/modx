# Derived from official mysql image (our base image)
FROM mysql:5.7
MAINTAINER ivan.fanchenko@gmail.com
# Add a database
ENV MYSQL_ROOT_PASSWORD=''
ENV MYSQL_DATABASE=modx
ENV MYSQL_USER=''
ENV MYSQL_PASSWORD=''
# Add the content of the sql-scripts/ directory to your image
# All scripts in docker-entrypoint-initdb.d/ are automatically
# executed during container startup
VOLUME ./mysql:/var/lib/mysql
COPY ./modx_init.sql /docker-entrypoint-initdb.d/
COPY ./testdb.sh /
RUN chmod 777 /testdb.sh
EXPOSE 3306
