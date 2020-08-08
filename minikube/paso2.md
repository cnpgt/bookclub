# Mostrando el dashboard #
  
Para exponer el dashboard ejecuta:  
`kubectl expose deployment/kubernetes-dashboard --name=dashboard-public --port=80 --target-port=9090 --type=NodePort -n kubernetes-dashboard`{{execute}}


Revisemos el puerto al que se conecto en los services:  
`kubectl get services -n kubernetes-dashboard`{{execute}}

Pues accederlo en la pestaña llamada *K8s Dashboard*  
  
https://[[HOST_SUBDOMAIN]]-YOURPORT-[[KATACODA_HOST]].environments.katacoda.com/

# Realizando troubleshooting a la conexión al Cluster #
Ver la versión de nuestro cliente:  
  
`kubectl version`{{execute}}  

Es importante configurar las credenciales de kubectl en *~/.kube/config*, sin ello no podrás conectarte al cluster. 
  
Ahora miremos el archivo de configuración para conectarnos:  
  
`kubectl config view`{{execute}}  

Ver los contextos disponibles de conexión:  
  
`kubectl config get-contexts`{{execute}}  


# Troubleshooting #
Ahora hagamos unas pequeñas pruebas del cluster, listando los nodos que tiene:  
  
`kubectl get nodes -o wide`{{execute}}
  
Ahora mostremos el estado de sus componentes si son saludables:  
  
`kubectl cluster-info`{{execute}}  

Ver el estado de algunos componentes:  
  
`kubectl get componentstatus`{{execute}}  
  
Eventos en el cluster:  
  
`kubectl get events`{{execute}}