Learn Symfony Projekt
=====================

Setup
-----
docker compose up -d
docker compose exec -u 1000 -it unit composer install

Dienste stoppen
---------------
docker compose stop

Dienste starten
---------------
docker compose start

Dienste löschen
---------------
docker compose down

Shell in den PHP-Container
--------------------------
docker compose exec -u 1000 -it unit bash

Symfony Console Command ausführen
---------------------------------
docker compose exec -u 1000 -it unit bin/console

Services
========

App http://localhost:8080

Mailcatcher http://localhost:1080
