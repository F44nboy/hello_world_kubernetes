# Hello Kubernetes

This project demonstrates how to deploy a simple "Hello World" application on Kubernetes.


After deployment you can Implement Advanced Features (Auto-scaling, Rolling Updates, Self-healing), if you want, with these commands:


Auto-scaling:
  ```bash
    kubectl autoscale deployment hello-kubernetes --cpu-percent=50 --min=1 --max=5
```
This command sets up horizontal pod autoscaling based on CPU utilization.

Rolling Updates:
  ```bash
    kubectl set image deployment/hello-kubernetes hello-kubernetes=your-dockerhub-username/hello-kubernetes:new-version
```
Kubernetes will perform a rolling update by gradually replacing the old pods with new ones.

Self-healing:
  ```bash
    kubectl delete pod <pod-name>
```
In a Deployment Kubernetes will automatically create a new pod to replace the deleted one.