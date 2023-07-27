FROM postgres:15.1-alpine

LABEL image.name="Postgres Database"
LABEL image.version="15.1"
LABEL image.description="An image of Postgres Database, which is used to store all the data and its relations in the voting app."
LABEL image.author="mmaziec"

COPY *.sql /docker-entrypoint-initdb.d/
EXPOSE 5432
