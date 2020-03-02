# config

# force remove all docker container and docker image
docker rmi -f $(docker image ls -a -q)
docker rm -f $(docker ps -a -q)
