# Task - Day 39


## Task 1

- installing jenkins on a ec2 machine with the help of a shell script using `user data` feature in ec2 creation advanced options
      
  Script: ( Here the AMI was amazon Linux.)
    
 ```
#!/bin/bash
sudo yum update -y
sudo yum install wget
sudo amazon-linux-extras install java-openjdk11
sudo amazon-linux-extras install epel -y
sudo wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins-ci.org/redhat/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
sudo yum install jenkins -y
sudo service jenkins start
sudo yum install jenkins
```
  
  
  
Screenshot:
  - User data script
  
  ![Screenshot 2023-03-02 at 1 08 06 PM](https://user-images.githubusercontent.com/101057601/222364184-dabb55f2-abd5-404d-bf77-e645c2b59fe7.png)
  
  - Jenkins portal on server
  
  ![Screenshot 2023-03-02 at 1 08 25 PM](https://user-images.githubusercontent.com/101057601/222364341-04ae04ca-b4a5-414a-b4a4-22e536697ad0.png)

  
  ## Task 2
  
  - Screenshots
 
 ![Screenshot 2023-03-02 at 1 28 31 PM](https://user-images.githubusercontent.com/101057601/222366883-5dd557f4-7360-46d9-ac9f-e4dfd922f097.png)
 
 ![Screenshot 2023-03-02 at 1 28 39 PM](https://user-images.githubusercontent.com/101057601/222366908-954fb9d1-ead2-4840-accd-36970d6b1de0.png)

  
