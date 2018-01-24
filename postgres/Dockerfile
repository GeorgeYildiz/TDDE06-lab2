FROM postgres:latest

ENV POSTGRES_DB my_database
COPY ./postgres/schema.sql /docker-entrypoint-initdb.docker/schema.sql
CMD ["psql", "-f", "/docker-entrypoint-initdb.docker/schema.sql", "my_database"]