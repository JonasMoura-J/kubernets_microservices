# kubernets_microservices
Subindo e gerenciando microserviços com kubernets

build do docker gateway:
docker build -t user_dock_hub/nome_build nome_microservice/.

colocar o build em um repositório do docker hub:
docker push user_dock_hub/nome_build


Minikube doc e instalação:
https://minikube.sigs.k8s.io/docs/start/?arch=%2Fwindows%2Fx86-64%2Fstable%2F.exe+download

minikube start
