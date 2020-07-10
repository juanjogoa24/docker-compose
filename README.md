Configuracion de los archivos docker compose que se usan para crear los contenedores que se necesitan.

Comados:
ejecutar en segundo plano, siempre abriendo un terminal en la ubicacion de la carpeta donde esta el archivo *.yml

$ docker-compose up -d

Postgres crear db en docker:

$ docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                     NAMES
05b3a3471f6f        postgres            "/docker-entrypoint.s"   1 seconds ago       Up 1 seconds        0.0.0.0:5432->5432/tcp    some-postgres

ingresar al contenedor en docker y crear la db:
$ docker exec -it 05b3a3471f6f bash
root@05b3a3471f6f:/# psql -U postgres
postgres-# CREATE DATABASE mytest;
postgres-# \q