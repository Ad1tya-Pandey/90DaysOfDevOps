# Task - Day 47 

- deployed a website on ec2

![Screenshot 2023-03-02 at 10 57 49 PM](https://user-images.githubusercontent.com/101057601/222529723-967e1452-ce06-4316-92f7-ae47cc38156b.png)


## Auto scaling 

### Steps taken :

- created a launch template and used AWS auto scaline guidance option during creation of the launch template from ec2 (with auto allocation of ipv4 public ip)

- created a Auto scaling group 
![Screenshot 2023-03-03 at 12 44 13 AM](https://user-images.githubusercontent.com/101057601/222531020-f454a75b-c37d-40f0-9ff4-43d1de852383.png)


- made multiple request using `blazemeter` which resulted into firing up of the last and the third instance as per the auto scaling group settings
 
final output:

![Screenshot 2023-03-03 at 12 42 22 AM](https://user-images.githubusercontent.com/101057601/222530132-fca8a5fc-7ac2-42fb-b4a6-c65e4d2d2f96.png)
