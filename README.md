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


### info about minikube cluster:
*kubectl cluster-info*
*Kubernetes control plane is running at https://192.168.49.2:8443*
*CoreDNS is running at https://192.168.49.2:8443/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy*

*To further debug and diagnose cluster problems, use 'kubectl cluster-info dump'.*


### kube dashboard token

link http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/

kubectl -n kubernetes-dashboard create token admin-user
eyJhbGciOiJSUzI1NiIsImtpZCI6IlMzU0lmbl9za19yVEFud2JlZGIydzJicW4zM0E1NFhSWXRZdTByckJMWG8ifQ.eyJhdWQiOlsiaHR0cHM6Ly9rdWJlcm5ldGVzLmRlZmF1bHQuc3ZjLmNsdXN0ZXIubG9jYWwiXSwiZXhwIjoxNjcwNzUwNTA3LCJpYXQiOjE2NzA3NDY5MDcsImlzcyI6Imh0dHBzOi8va3ViZXJuZXRlcy5kZWZhdWx0LnN2Yy5jbHVzdGVyLmxvY2FsIiwia3ViZXJuZXRlcy5pbyI6eyJuYW1lc3BhY2UiOiJrdWJlcm5ldGVzLWRhc2hib2FyZCIsInNlcnZpY2VhY2NvdW50Ijp7Im5hbWUiOiJhZG1pbi11c2VyIiwidWlkIjoiMGY1M2EzNjEtNWNlYS00ZWI0LWIxMDQtMjZhNTI1ODI0ZTZiIn19LCJuYmYiOjE2NzA3NDY5MDcsInN1YiI6InN5c3RlbTpzZXJ2aWNlYWNjb3VudDprdWJlcm5ldGVzLWRhc2hib2FyZDphZG1pbi11c2VyIn0.HcuHvdtsGmftcygsuai0Q_ewfdFJn8aUSDl9DchEgZZaOgOIBFtYuy66gXoFgb9LXDnRez08ZEUu67XScVmEec_Vdl8nH2l-hVpOBf_cogksb7M9yxvKxMuIi8IGSetindNREw6ucj9ihUZJ6JSqvON01xXNd30dL25Qi8e1nRVUCY3g1d-i2m-4F3Tcs32yihiTiGr7Q5bDDKDInGwEfDdw3ozutc0TFyyRY4iIOQodpyN06VTZ_Ax0tKdsb9rbm0kZjVu3R5JO8aM1l-wyVBYWJRWbRKFTEOxYFFAImvNDLOT4yRWdZv1VCdgt3uq90oxogK9yDEkdygf5aBbdOA

** $ kubectl get pod -n kubernetes-dashboard **
NAME                                         READY   STATUS    RESTARTS   AGE
dashboard-metrics-scraper-64bcc67c9c-2pkgw   1/1     Running   0          17m
kubernetes-dashboard-66c887f759-x4cxz        1/1     Running   0          17m
