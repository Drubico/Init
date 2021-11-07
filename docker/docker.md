
https://hub.docker.com/u/dilverpro
https://docs.docker.com/engine/install/linux-postinstall/

sudo usermod -aG docker drubico

# si tengo un proyecto de npm por ejemplo 
```
sudo docker build -t lessa-frontend .

sudo docker run -it -p 3000:3000 lessa-frontend
```
docker rm -vf $(docker ps -aq)

docker rm -vf $(docker images -aq)

docker rmi <<name>><<or id>>

docker rmi d1be65f9a308

# Subir imagen :
```
sudo docker build -t lessa-frontend .

docker push dilverpro/lessa-frontend:v1 # subimos la imagen en su version 1 
docker push dilverpro/lessa-frontend:v2 # subimos la imagen en su version 2

docker tag 201a126bfdb6 dilverpro/lessa-frontend:v1
```
# Correr imagen en live
```
sudo docker build -t lessa-frontend .

docker run -v /media/drubico/Drubi/Git_CLONES/MR_Devart/LESSA_Frontend:/app/ -it -p 3000:3000 lessa-frontend

```
# Docker Compose

```
docker-compose up
docker-compose down
```
## -d es para background
```
docker-compose up -d
docker-compose down -d
```