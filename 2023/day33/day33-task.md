# Day33 - Task

- Deployment.yaml
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

Namespace number 2 in the attached picture below was created after the deployment file was executed.

![Screenshot 2023-02-02 at 11 03 33 PM](https://user-images.githubusercontent.com/101057601/216399220-ea30e702-5795-469b-9512-e6aeb023e4b1.png)

ps: services would be used to expose these pods to internet , there are 4 types of services which could help us achieve this objective as per kubernetes' official documentation.
