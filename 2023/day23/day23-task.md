# Task - Day 23
 
 - In order to complete the mentioned tasks I've :
 
 -> Created a declarative multistage pipeline for a Nodejs web application with `Code` , `build` , `push` , `test` and `deploy` stage in it.
 
 ## Pipeline Script
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
 Also in accomplishing the outcome i had to use ibuilt plugins of jenkins like `Github itegration` and `Credential binding`.
 
 Outcome:
 
 ![Screenshot 2023-01-23 at 11 57 38 PM](https://user-images.githubusercontent.com/101057601/214120338-b347f70b-9dbb-424a-ad07-1d721268fe13.png)

 
 
