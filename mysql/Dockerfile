# FROM mysql:8.0
# ENV MYSQL_ROOT_PASSWORD=ExpenseApp@1 
# ADD scripts/*.sql /docker-entrypoint-initdb.d
#     # MYSQL_DATABASE=transaction \
#     # MYSQL_USER=expense \
    # MYSQL_PASSWORD=ExpenseApp@1 

# FROM mysql:8.0
# ENV MYSQL_ROOT_PASSWORD=ExpenseApp@1
# ADD scripts/*.sql /docker-entrypoint-initdb.d

FROM mysql:8.0
ENV MYSQL_ROOT_PASSWORD=ExpenseApp@1
RUN groupadd expense && \
    useradd -g expense expense && \
    chown -R expense:expense /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d
ADD scripts/*.sql /docker-entrypoint-initdb.d
USER expense


# FROM mysql:8.0
# ENV MYSQL_ROOT_PASSWORD=ExpenseApp@1
# RUN groupadd expense && \
#     useradd -g expense expense && \
#     chown -R expense:expense /docker-entrypoint-initdb.d
# ADD scripts/*.sql /docker-entrypoint-initdb.d
#USER expense
    # MYSQL_DATABASE=transactions \
    # MYSQL_USER=expense \
    # MYSQL_PASSWORD=ExpenseApp
    #/var/lib/mysql /var/run/mysqld