# Day 34 - Task

## Services in Kubernetes:
1. clusterIP
2. NodePort
3. Load Balancer
4. Ingress (requires a domain name)

### service.yaml file (with minimal changes in each type)
```
apiVersion: v1
kind: Service
metadata:
  name: django-todo-service
  namespace: django-todo-app
spec:
  type: LoadBalancer
  selector:
    app: django-app
  
  ports:
    - port: 80
      targetPort: 8000
      protocol: TCP
```

### Screenshots :

- ClusterIp  : accessible inside the node.
- 
![Screenshot 2023-02-04 at 10 38 38 PM](https://user-images.githubusercontent.com/101057601/216781105-0ef09fe1-f176-4dc6-bcce-a0fe20cf16e4.png)

- NodePort  : accessible from outside the node using Node IP and designated port.
![Screenshot 2023-02-04 at 10 43 16 PM](https://user-images.githubusercontent.com/101057601/216781186-4ba8f481-377b-4456-8534-859f94e80bce.png)

- Load Balancer : for direct exposing of service to the internet
![Screenshot 2023-02-04 at 10 53 50 PM](https://user-images.githubusercontent.com/101057601/216781203-da818ddc-5679-45fe-a4da-7ace6f1ca059.png)

ps : Read this [article](https://medium.com/google-cloud/kubernetes-nodeport-vs-loadbalancer-vs-ingress-when-should-i-use-what-922f010849e0) for a quick refresher to the concept.
