# Mostrando el dashboard y realizando troubleshooting al Cluster #
Kubernetes tiene un dashboard el cual podemos instalar.  Para mostrarlo en Minikube utiliza el comando:

`minikube dashboard`{{execute}}

Pues accederlo en la pestaña llamada *K8s Dashboard*

Ahora hagamos unas pequeñas pruebas del cluster, listando los nodos que tiene:  
  
`kubectl get nodes -o wide`{{execute}}
  
Ahora mostremos el estado de sus componentes si son saludables:  
  
`kubectl cluster-info`{{execute}}  

Versión de nuestro cliente del API:  
  
`kubectl version`{{execute}}  

Algunos otros detalles del cluster:  
  
`kubectl get componentstatus`{{execute}}  

Ver el archivo de configuración para conectarnos:  
  
`kubectl config view`{{execute}}  

Ver los contextos disponibles de conexión:  
  
`kubectl config get-contexts`{{execute}}  
  
Describir un nodo:  
  
`kubectl describe node minikube`{{execute}}

Eventos en el cluster:  
  
`kubectl get events`{{execute}}