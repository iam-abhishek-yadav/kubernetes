# Creating first pod

1. [Install Minikube](https://minikube.sigs.k8s.io/docs/start/)

2. [Install kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

3. **Create pod.yaml file:**
    ```yaml
    apiVersion: v1
    kind: Pod
    metadata:
        name: nginx
    spec:
        containers:
        - name: nginx
        image: nginx:1.14.2
        ports:
        - containerPort: 80
    ```
 
4. **Start cluster**
    ```bash
    minikube start
    ```
 
5. **Create Pod**
    ```bash
    kubectl create -f pod.yaml
    ```
 
6. **Verify Pod Creation**
    ```bash
    kubectl get pods
    ```
 
7. **Describe Pod**
    ```bash
    kubectl describe pod nginx
    ```
 
8. **Delete Pod**
    ```bash
    kubectl delete pod nginx
    ```

