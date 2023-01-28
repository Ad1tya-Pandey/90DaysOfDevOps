# Day28 - Task

- created a agent , connected it to the node for jenkins using ssh and successfully deployed application onto agent from the master node using declarative CI/CD pipeline.
- Screenshots:
![Screenshot 2023-01-29 at 12 26 25 AM](https://user-images.githubusercontent.com/101057601/215286048-ebdcea38-4ad8-4c98-a348-4388b903a3eb.png)
![Screenshot 2023-01-29 at 12 27 15 AM](https://user-images.githubusercontent.com/101057601/215286050-a468b033-cb6d-4d1b-838d-0cac7547e464.png)


## key points to remember while configuring Jenkins agent :
1. All machines need to have same version of java installed on them for communication to take place.
2. install docker on agent and provide with necessary privilege.
3. copy the public key of master in agent's `authorized-key` file and put the private key of master in credentials of jenkins as a env to provide for the agent to accomplish ssh connection.
