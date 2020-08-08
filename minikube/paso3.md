# Creando una aplicación #
Crearemos un pod, que es la unidad más pequeña de despliegue en Kubernetes, un pod contiene un container al menos, pueden existir varios containers dentro de un pod.  

Para crear un pod ejecutamos:  
  
`kubectl run --image=busybox -it --rm --restart=Never -- sh echo "hola mundo"`{{execute}}
  
Listo ya hemos creado nuestro primer pod en el cluster

Ahora creemos un servidor web que podamos acceder, primero creamos un pod con el comando:
  
`kubectl run nginx --image=nginx --restart=Never`{{execute}}  
  
Ahora hacemos público el servicio creando un service con el comando:
`kubectl expose pod nginx --name=nginx-public --port=80 --target-port=80 --type=NodePort`{{execute}}


