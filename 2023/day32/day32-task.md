# Day32 - Task

* Deployment.yaml :
```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: django-app-deployment
  labels:
    app: django-app
  namespace: django-todo-app

spec:
  replicas: 2   
  selector:
    matchLabels:
      app: django-app
  template:
    metadata:
      labels:
        app: django-app

    spec:
      containers:
      - name: django-todo-ctr
        image: trainwithshubham/django-todo:latest
        ports:
        - containerPort: 8000 
```
 
 ## Understanding `deployment.yaml` :
 1. `kind` : to specify the kind of file 
 2. `metadata`: which would carry the basic info of deployment like name , labels , namespace.
 3. `spec`: spec 1 is for specification of deployment properties (replicas etc)
 4. `spec` : sepc 2 is for pod creation , using spec two we can directly create pods in the deployment file itself rather than writing seperate `pod.yaml`

Output after applying the file using `kubectl apply -f podname -n namespace`:
 
 ![Screenshot 2023-02-02 at 7 12 27 PM](https://user-images.githubusercontent.com/101057601/216340884-c25353f0-4716-4aa5-8c55-5c8a2e0274ab.png)
