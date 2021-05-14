## список скаченных обрaзов
docker images

## собрать образ докера
docker build-t hello-world .

## запустить контейнер
docker run b6269461979a
docker run --name hello -d hello-world

## чтобы контейнер после запуска удалился
docker run --name hello -d --rm hello-world
docker run --rm --name web web-hello
docker run --rm --name web -p 8080:8080 web-hello
docker run --rm --name web -p 8080:8080 -e TZ=Europe/Moscow web-hello
 
## просмотр контейнеров
docker ps
e — в том числе остановленные
docker ps -a -q — только айдишники

## остановка контейнера
docker stop hello
docker stop $(docker ps -qa)

## удаление контейнера
docker rm b6269461979a
docker rm $(docker ps -qa)

## удаление image
docker rmi 3da2468ae0f4

## удалить все образы с none
docker images -q
docker rmi $(docker images -q)
docker rmi -f $(docker images -a -q)

## простой докерфайл
FROM python:3.7.4-alpine

RUN mkdir -p /usr/src/app/
WORKDIR /usr/src/app/

COPY . /usr/src/app/
RUN pip3 install -r requirements.txt

EXPOSE 8080

CMD ["python", "app.py"]


## монтирование директории
docker run --rm --name web -p 8080:8080 -e TZ=Europe/Moscow -v /media/orlovkn/work/cloud/practice/docker/resources:/usr/src/app/resources web-hello


## установка зависимостей
pip install -r requirements.txt


## список volume
docker volume ls

## создать volume
docker volume create web

## запуск с указанием volume
docker run --rm --name web -p 8080:8080 -v web:/usr/src/app/resources web-hello

## удалить volume
docker volume rm $(docker volume ls)





FROM python:3.7.4-alpine as base

#FROM base as builder
FROM base
RUN apk add postgresql-dev gcc python3-dev musl-dev
RUN mkdir /install
WORKDIR /app
COPY requirements.txt .
#RUN pip3 install -r requirements.txt --prefix=/install
RUN pip3 install -r requirements.txt
COPY . .

#FROM base
#WORKDIR /app
#COPY --from=builder /app .
#COPY --from=builder /install /usr/local


https://github.com/andruwwwka/rebus-hackathon-final/blob/master/docker-compose.yaml





https://docs.docker.com/compose/reference/ Compose command-line reference


## от елисеева
docker run --rm -v ${PWD}/manager:/app --workdir=/app.php php:7.2-cli ls
docker run --rm -v ${PWD}/manager:/app --workdir=/app.php php:7.2-cli php bin/app.php
echo ${PWD}

docker run --rm -v ${PWD}/manager/public:/var/www/html -p 8080:80 php:7.2-apache

сделать Makefile, прописать в нём команду
```
cli:
	docker run --rm -v ${PWD}/manager:/app --workdir=/app.php php:7.2-cli php bin/app.php
apache:
	docker run --rm -v ${PWD}/manager/public:/var/www/html -p 8080:80 php:7.2-apache
```

запуск
```
make cli
make apache
```


Image for service php74-service was built because it did not already exist. To rebuild this image you must use `docker-compose build` or `docker-compose up --build`.


запуск
docker-compose up -d --build

зайти в контейнер
docker exec -it php74-container bash

остановить все процессы
docker-compose down


If lsof -i :5432 doesn't show you any output, you can use sudo ss -lptn 'sport = :5432' to see what process is bound to the port.

Proceed further with kill <pid>


sudo service postgresql stop


docker-compose run --rm php74-service php bin/console doctrine:database:create


docker logs mysql8-container


DATABASE_URL="mysql://admin:secret@s5-app-mysql:3306/s5_db?serverVersion=8"



docker run -it redis

docker inspect

