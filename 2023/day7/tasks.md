# Task for Day 7
- wrote a blog as mentioned in the tasks and explained the installation process as well as relevant terminologies.
the link to it:<br>
https://heckit.hashnode.dev/installing-docker-on-linux

- systemD is a service while systemctl is the command line utility used to control it

- In the context of Docker, a service is a container that is running as part of a Docker swarm, which is a group of Docker nodes that are running together as a cluster. A service runs a specified number of replicas of a container, and ensures that the desired number of replicas are running at all times.

Systemctl is not typically used to control services in Docker, as systemd is not generally used in the same way as it is in a traditional Linux environment. Instead, Docker provides its own command-line interface (CLI) for managing services. The docker service command can be used to create, update, and manage services in a Docker swarm. For example, you can use the docker service create command to create a new service, or the docker service scale command to increase or decrease the number of replicas of a service.
