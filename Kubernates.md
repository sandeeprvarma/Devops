##Basic commands
1. How to switch context
   ```
   aws eks update-kubeconfig --name=<namespce> --profile <aws_profile>
   ```
2. get current context of k8
   ```
   kubectl config current-context
   ```
3. create a new pod with nginx image 
  ```
  kubectl run pod_name --image=nginx
  ```
4. get all ready pods
  ```
  kubectl get pods
  ```
5. Additional info such as where node is running and ip address etc
  ```
  Kubectl get pods -o wide
  ```
6. Provide detailed infor of pod
  ```
  kubctl describe pod <pod_name>
  ```
7. Delete pod using pod name
```
  kubectl delete pod <pod_name>
```
8. Get deployments
```
  Kubctl get deployments
```
9. how all pods, deployments and replicasets
```
  kubectl get all
```
10. Some Important replicaset related commands:
```
Kubectl get replicaset

kubectl replace f replicaset-def.yml (to scale using yml file)

kubectl scale --replicas=6 -f replica-def.yml

kubectl scale --replicas=6  replicaset replicaset_name

kubectl edit replicaset replicaset_name
```
11. Get list if services
```
  kubectl get services
```
12. Describe selected service in detail
```
  kubectl describe service kubernetes
```
13. Get logs of pod using podname
```
  kubectl logs -n kube-system <metrics-server-pod-name>
```
   
