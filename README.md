# kubernets_microservices
Subindo e gerenciando microserviços com kubernets

build do docker gateway:
docker build -t user_dockerhub/java-gateway-k8s:v1 gateway/. ; docker build -t user_dockerhub/java-pedidos-k8s:v1 pedidos/. ; docker build -t user_dockerhub/java-pagamentos-k8s:v1 pagamentos/. ; docker build -t user_dockerhub/java-server-k8s:v1 server/.

colocar o build em um repositório do docker hub:
docker push user_dock_hub/nome_build


Minikube doc e instalação:
https://minikube.sigs.k8s.io/docs/start/?arch=%2Fwindows%2Fx86-64%2Fstable%2F.exe+download

minikube start

minikube addons list

minikube addons enable csi-hostpath-driver

APLICANDO AS CONFIGS DO K8s e criando pods

kubectl apply -f k8s/volumes.yaml -f k8s/mysql.yaml -f k8s/secrets.yaml -f k8s/configmap.yaml -f k8s/app.yaml -f k8s/loadbalancer.yaml

Abrir o tunnel:
minikube tunnel --bind-address=IP