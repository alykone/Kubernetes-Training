# Kubernetes-Training

#les principales etapes du projet

git clone https://github.com/alykone/Kubernetes-Training.git

cd Kubernet-training

# Creation des repertoires pour le stockage des données persistentes
mkdir -p /data/
mkdir /data/data-wp

#Deploiement MySQL
kubectl apply -f mysql-deployment.yml
#Configuration du service MySQL ClusterIP port 3306
kubectl apply -f service-mysql.yml

#Deploiement wordpress
kubectl apply -f wordpress-deployment.yml
#Configuration du service WordressL NodePort port 30001
kubectl apply -f service-wordpress.yml
