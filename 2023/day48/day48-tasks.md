# Running a docker image on `ECS using Fargate`

- Steps involved :
                   1) creating a docker image.  
                   2) pushing image to `ECR` (by creating a repository on ECR and following the commands in 'ECR push' menu).  
                   3) creating a `Cluster` with the help of `Fargate`.  
                   4) creating a task for running our container using the image from either ECR , dockerhub.  
                   5) creating a service to run the new task that we created earlier. 
                   
                   
## Screenshot

- cluster with task running inside it (a cluster can contain one or more than one containers)
![Screenshot 2023-03-03 at 11 13 58 PM](https://user-images.githubusercontent.com/101057601/222793437-0d3d57ce-d095-41ee-ac89-80eddf537fc4.png)

- cluster ip with nginx running on it
![Screenshot 2023-03-03 at 11 14 10 PM](https://user-images.githubusercontent.com/101057601/222793594-f1d68e1e-bae8-4612-8cc2-0e985c45fc8b.png)
