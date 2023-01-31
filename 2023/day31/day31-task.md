# Day31 - Task

- created a file pod.yaml 

### pod.yaml
```
apiVersion: v1
kind: Pod
metadata:
  name: django-todo-pod
  namespace: django-todo-app
spec:
  containers:
    - name: django-todo-ctr
      image: trainwithshubham/django-todo:latest
      ports:
        - containerPort: 8001


```
- executed it using the command ` kubectl apply -f pod.yaml `

Output:

![Screenshot 2023-01-31 at 11 15 49 PM](https://user-images.githubusercontent.com/101057601/215841411-3de22bbd-09bb-4ec0-91fd-7cad201a021c.png)
