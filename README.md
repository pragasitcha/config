# config

## Docker

docker ps -a 

docker image ls 

docker build -f {{Dockerfile}} -t {{imagename}}:{{imagetag}} . (<< dot also a part of command.)

{{imagename}}:{{imagetag}} ex. image:0.0.1

docker run -it -d -p 8080:8080 {{imagename}}:{{imagetag}} 

docker stop {{container id}}

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

kubectl create -f {{resourcefile}}

kubectl delete -f {{resourcefile}}

kubectl describe pods

kubectl describe pods -n {{namespace}}

kubectl logs {{podsname}} 

kubectl logs -f {{podsname}} 

kubectl exec -it {{podsname}} /bin/bash

kubectl exec -it {{podsname}} /sh

# Clean re install minikube 
remove /etc/kubernetes/ 
remove /var/lib/kubelet 
remove /var/lib/minikube 
remove /root/.kube
remove /root/.minikube
remove /usr/bin/minikube
remove /usr/bin/kubectl

remove docker image and container 

#if cannot container hang and status = create . we need  manual delete.

remove all docker volume 

#if cannot container still hang and status = RemovalInProgress . we need  manual delete.
change status of container /var/lib/docker/containers/[longcontainerid]/config.v2.json  change RemovalInProgress to false 

systemctl daemon-reload && systemctl restart docker

# try delete container -f again.

# permanently save the namespace for all subsequent kubectl commands in that context.
kubectl config set-context --current --namespace=ggckad-s2

# Export Centos Systemlog as text.
journalctl  --no-pager --since "2018-08-30 14:10:10"

journalctl  --no-pager --since "2018-08-30" > exportlog.txt
