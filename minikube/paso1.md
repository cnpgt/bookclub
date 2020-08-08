# Instalando el cluster y el dashboard#
Para comenzar revisaremos la versión de nuestro minikube con *minikube version*  

`minikube version`{{execute}}

Ahora iniciaremos nuestro cluster ejecutando el siguiente comando:  

`minikube start`{{execute}}

Ahora ya tenemos corriendo nuestro cluster en este pequeño ambiente.
  
Kubernetes tiene un dashboard el cual podemos instalar.  Para mostrarlo en Minikube utiliza el comando:

`minikube dashboard &`{{execute}}