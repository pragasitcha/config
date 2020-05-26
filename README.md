# config

## Docker

docker ps -a 

docker image ls 

docker build -f {{Dockerfile}} -t {{imagename}}:{{imagetag}} . (<< dot also a part of command.)
{{imagename}}:{{imagetag}} ex. image:0.0.1

docker run -it -d -p 8080:8080 {{imagename}}:{{imagetag}} 

docker rm {{container id}}

docker rm -f {{container id}}

docker rmi {{image id}}

docker rmi -f {{image id}}

docker save {{image repo}} | gzip > {{export name}}.tar.gz

docker load {{export name}}.tar.gz

docker log {{container id}}.tar.gz

docker log -f {{container id}}.tar.gz

docker exec -it {{container name}} /bin/bash

docker exec -it {{container name}} /bin/bash

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

