Started by user admin
[Pipeline] Start of Pipeline
[Pipeline] node
Agent mypod-54dx6 is provisioned from template mypod
---
apiVersion: "v1"
kind: "Pod"
metadata:
  labels:
    jenkins: "slave"
    jenkins/label-digest: "46dd2021555fb3d1368ecfa0973fda2edff3af87"
    jenkins/label: "anytask"
  name: "mypod-54dx6"
  namespace: "jenkins"
spec:
  containers:
  - args:
    - "9999999"
    command:
    - "sleep"
    image: "python"
    imagePullPolicy: "IfNotPresent"
    name: "python"
    resources:
      limits: {}
      requests: {}
    tty: false
    volumeMounts:
    - mountPath: "/home/jenkins/agent"
      name: "workspace-volume"
      readOnly: false
    workingDir: "/home/jenkins/agent"
  - env:
    - name: "JENKINS_SECRET"
      value: "********"
    - name: "JENKINS_AGENT_NAME"
      value: "mypod-54dx6"
    - name: "JENKINS_NAME"
      value: "mypod-54dx6"
    - name: "JENKINS_AGENT_WORKDIR"
      value: "/home/jenkins/agent"
    - name: "JENKINS_URL"
      value: "http://192.168.0.137:8080/"
    image: "jenkins/inbound-agent:4.11-1-jdk11"
    name: "jnlp"
    resources:
      limits: {}
      requests:
        memory: "256Mi"
        cpu: "100m"
    volumeMounts:
    - mountPath: "/home/jenkins/agent"
      name: "workspace-volume"
      readOnly: false
  hostNetwork: false
  nodeSelector:
    kubernetes.io/os: "linux"
  restartPolicy: "Never"
  volumes:
  - emptyDir:
      medium: ""
    name: "workspace-volume"

Running on mypod-54dx6 in /home/jenkins/agent/workspace/pipeline-2
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Run python)
[Pipeline] container
[Pipeline] {
[Pipeline] sh
+ python3 --version
Python 3.11.1
+ sleep 50
[Pipeline] }
[Pipeline] // container
[Pipeline] }
[Pipeline] // stage
[Pipeline] }
[Pipeline] // node
[Pipeline] End of Pipeline
Finished: SUCCESS