
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
