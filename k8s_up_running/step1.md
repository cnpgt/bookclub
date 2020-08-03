## Troubleshooting the cluster ##
With the kubectl command you can list the nodes of your cluster  
`kubectl get nodes`{{execute HOST1}}  
You can also get the description on each node  
`kubectl describe nodes`{{execute HOST1}}  
You can get only the IPs with the next command  
`kubectl describe nodes | grep ExternalIP`{{execute HOST1}}  
