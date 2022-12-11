## In this project shown cluster Minikube in Virtualbox with Jenkins and k8s slaves.

*Virtualhost ip:192.168.0.137*

### Settings from Virtualbox jenkins-master server 
![image](https://user-images.githubusercontent.com/44971394/206868126-cb391462-b07f-49ea-b774-33eec3271095.png)


### Output 
![image](https://user-images.githubusercontent.com/44971394/206870130-522b13b5-fa16-4901-9bec-8433f73fb2ae.png)


### Jenkins output
nick@nick-VirtualBox:~$ jenkins --version
2.375.1

![image](https://user-images.githubusercontent.com/44971394/206870258-87ef3732-0fea-4bb0-afb2-1d3366b35157.png)


info about minikube cluster:
*kubectl cluster-info
Kubernetes control plane is running at https://192.168.49.2:8443
CoreDNS is running at https://192.168.49.2:8443/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy

To further debug and diagnose cluster problems, use 'kubectl cluster-info dump'.*