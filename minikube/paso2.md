# Mostrando el dashboard y realizando troubleshooting al Cluster #
Kubernetes tiene un dashboard el cual podemos instalar.  Para mostrarlo en Minikube utiliza el comando:

`minikube dashboard`{{execute}}

Este puedes accederlo en:


Ahora hagamos unas pequeñas pruebas del cluster, listando los nodos que tiene:  
  
`kubectl get nodes -o wide`{{execute}}
  
Ahora mostremos el estado de sus componentes si son saludables:  
  
`kubectl cluster-info`{{execute}}  

Versión de nuestro cliente del API:  
  
`kubectl version`{{execute}}  

Algunos otros detalles del cluster:  
  
`kubectl get componentstatus`{{execute}}  
  
`kubectl config view`{{execute}}  
  
`kubectl config get-contexts`{{execute}}  
  
Describir un nodo:  
  
`kubectl describe node minikube`{{execute}}

Eventos en el cluster:  
  
`kubectl get events`{{execute}}