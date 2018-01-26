FROM postgres:latest

ENV POSTGRES_DB postgres
ENV POSTGRES_USER postgres
COPY ./schema.sql /docker-entrypoint-initdb.docker/schema.sql
CMD ["psql", "-f", "/docker-entrypoint-initdb.docker/schema.sql", "my_database"]
CMD ["postgres"]