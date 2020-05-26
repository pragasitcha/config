# config

## Docker

docker ps -a 

docker image ls 

docker rm {{container id}}

docker rm -f {{container id}}

docker rmi {{image id}}

docker rmi -f {{image id}}

## force remove all docker container and docker image

docker rmi -f $(docker image ls -a -q)

docker rm -f $(docker ps -a -q)

## Kube Note

kubectl get pods

kubectl get svc

kubectl get ingress

kubectl get configmap

kubectl get secret

kubectl get pv

kubectl get pvC

kubectl get pods -A

kubectl get pods -n {{namespace}}

kubectl describe pods

kubectl describe pods -n {{namespace}}

kubectl logs {{podsname}} 

kubectl logs -f {{podsname}} 

kubectl exec -it {{podsname}} /bin/bash

kubectl exec -it {{podsname}} /sh

