# Day30 - Task

1. What is Kubernetes? Write in your own words and why do we call it k8s?

- Kuberenetes is a container orchestrator it provides a way to schedule and manage containers (such as Docker) on a cluster of computers, ensuring that the containers are always available and able to automatically recover from failures it is called `k8s` because there are in total 8 letters in the word `kuberenetes` between 'k' and 's'


2. What are the benefits of using k8s?

- Scalability: Automatically scale application containers based on demand.
  High Availability: Automatically manage the availability of applications.
  Portability: Deploy applications consistently across on-premises, cloud, and hybrid environments.
  Automated Rollouts and Rollbacks: Roll out and roll back changes to applications with ease.
  Resource Optimization: Allocate resources efficiently and automatically to applications.
  Self-Healing: Automatically recover from failures and keep applications running.
  Declarative Configuration: Describe desired state and let Kubernetes manage the current state.
  
3. Explain the architecture of Kubernetes

- Kubernetes architecture consists of a cluster of nodes, each containing the following components:

  API Server: The central management component of a cluster, serving the API for read and write access to the cluster.
  etcd: A distributed key-value store storing the configuration data for the cluster.
  Scheduler: Determines which node an application should run on.
  Controller Manager: Manages the state of the cluster, such as replicating controllers and handling node failures.
  Kubelet: An agent that runs on each node, responsible for ensuring containers are running and responding to changes in the desired state.
  Container Runtime: The low-level software responsible for starting and stopping containers on a node, such as Docker.
  Pods: The smallest deployable units in Kubernetes, containing one or more containers.
  Services: A stable endpoint for pods, abstracting the underlying pods and providing load balancing.
  Volume: A way to persist data in containers across pod restarts.
  Namespaces: A way to divide cluster resources among multiple users or teams.

  These components work together to manage the deployment, scaling, and operation of containerized applications in a cluster.

4. What is Control Plane?

- Control Plane is a set of components in a Kubernetes cluster responsible for maintaining the desired state of the cluster. The Control Plane includes `API server, etcd, control manager, scheduler`

5. Write the difference between kubectl and kubelets.

- kubectl: A command-line tool for communicating with a Kubernetes cluster, used for managing and administering the cluster. It allows users to deploy, inspect, and manage their applications and resources within the cluster.
  kubelet: An agent that runs on each node in the cluster and is responsible for managing the containers and ensuring they are running and healthy. The kubelet communicates with the API server to receive information about the desired state of the cluster and takes action to ensure the actual state matches the desired state.

6. Explain the role of the API server.

- The API Server is a central component in a Kubernetes cluster that serves as the control plane, exposing the Kubernetes API and coordinating the actions of other components to maintain the desired state of the cluster. It validates and persists cluster state and communicates with other components, such as the controller manager and scheduler, to ensure the correct operation of the cluster.


