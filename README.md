1 - docker build -t node-docker .
2 - docker run -p 3333:3333 node-docker
3 - docker exec -it namecontainer /bin/bash

4 - docker-compose up
5 - docker-compose up -d
6 - docker logs node-docker -f
7 - docker-compose stop
8 - docker-compose down


docker-compose up - create
docker-compose down - delete
docker-compose start - start
docker-compose stop - stop


docker inspect --format='{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' node-docker
172.19.0.2
docker inspect --format='{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' post-compose
172.19.0.3

docker exec node-docker cat /etc/hosts

docker exec post-compose cat /etc/hosts
