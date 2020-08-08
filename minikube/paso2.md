# Mostrando el dashboard y realizando troubleshooting al Cluster #
Kubernetes tiene un dashboard el cual podemos instalar.  Para mostrarlo en Minikube utiliza el comando:

`minikube dashboard`{{execute}}

Este puedes accederlo en:


Ahora hagamos unas pequeñas pruebas del cluster, listando los nodos que tiene:  
  
`kubectl get nodes -o wide`{{execute}}
  
Ahora mostremos el estado de sus componentes si son saludables  
  
`kubectl cluster-info`{{execute}}