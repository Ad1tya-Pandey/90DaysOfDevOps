# Day24 - Task

- [Associated Github repository](https://github.com/Ad1tya-Pandey/node-todo-cicd.git/)

## Pipeline script
```
pipeline {
    agent any 
    stages{
        stage('Code'){
            steps{
            git url: 'https://github.com/Ad1tya-Pandey/node-todo-cicd.git', branch: 'master'
            }
        }
        stage('build'){
            steps{
                sh 'docker build . -t ad1tyapandey/node-todo-test:latest'
                 
                
            
            }
        }
        stage('push '){
            steps{
                 withCredentials([usernamePassword(credentialsId: 'Dockerhub', passwordVariable: 'DOCKER_PASSWORD', usernameVariable: 'DOCKER_USERNAME')]) {
                    // Deploy the code to Dockerhub
                    sh "docker login -u $DOCKER_USERNAME -p $DOCKER_PASSWORD"
                    sh "docker push  ad1tyapandey/node-todo-test:latest"
                }
                

            }
        }
        stage('Test'){
            steps{
                echo "testing the build"
            }
        }
        stage('Deploy'){
            steps{
                sh "docker-compose down && docker-compose up"
            }
        }
        
    }
    
}
```
- Screenshot

![Screenshot 2023-01-25 at 12 03 40 AM](https://user-images.githubusercontent.com/101057601/214378856-897a608e-7de9-4821-8fd4-b8a4ec0a1e41.png)

