## Orchestrator

More information about the project
[here](TASK.md)


И так что мы имеем на данный момент!
Готовый docker-compose.yml откуда загружаем все наши docker images from docker hub!

Задача развернуть наш проект на кубернетис! 
Так как у меня уже есть установленный миникуб в докере. 

Я начну со структуры папок 


#### 1. Kubernetes Object for billing-app
1.	**Deployment**: Defines the billing-app container, sets environment variables, and handles replica settings.
2.	**Service**: Exposes the billing-app Deployment to the cluster (or optionally externally).
3.	**ConfigMap**: Stores environment variables for non-sensitive configuration.
4.	**Secret**: Manages sensitive environment variables like database and RabbitMQ credentials.
5.	**Ingress** (Optional): Configures external access if needed, typically through a load balancer or ingress controller.




kubectl delete all --all -n default
kubectl delete secret --all
kubectl delete configmap --all

kubectl apply -f k8s --recursive