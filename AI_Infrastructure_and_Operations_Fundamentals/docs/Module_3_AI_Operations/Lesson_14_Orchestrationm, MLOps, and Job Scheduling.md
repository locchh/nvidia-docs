# Orchestrationm, MLOps, and Job Scheduling

Here’s the content formatted according to your specified agenda and objectives:

## Agenda
In this unit, we will cover:
- Overview of Orchestration and Scheduling
- Kubernetes
- MLOps
- SLURM

## Objectives
By the end of this unit, you will be able to:
- Describe the difference between orchestration and scheduling
- Describe common tools used for orchestration and scheduling
- Discuss the value of MLOps tools

## Overview of Orchestration and Scheduling
Welcome to Unit 14. In this unit, we'll be covering orchestration and job scheduling. We will give an overview of orchestration and scheduling, discussing Kubernetes and machine learning operations (MLOps), as well as the Slurm scheduler.

### Concepts of Orchestration and Scheduling
Container orchestration is a way to automate operations related to containers. Orchestration tools handle these tasks based on the needs of the environment being managed. 

- **Scheduling**: The process of assigning workloads to available compute resources. 
- **Orchestration**: Container-based, designed for microservices, and can scale based on inferencing needs. 
- **Scheduling**: Bare-metal based, designed for high-performance computing, and supports containers. 

### Key Differences
- Orchestration requires additional meta schedulers for advanced features, while schedulers have built-in advanced features like priority and preemption.
- Orchestration manages entire workflows and processes, whereas scheduling focuses on assigning tasks and jobs to available resources.
- Orchestration does load balancing to distribute traffic across containers, while scheduling determines hosts with the right resources to run containers.

## Kubernetes
Kubernetes is an open-source container orchestration system for automating software deployment, scaling, and management. Originally designed by Google, the Cloud Native Computing Foundation now maintains the project.

- **Container-Based Jobs**: Defined as specific commands to run on nodes that require certain resources (e.g., a CUDA container running `nvidia-smi` on a node with a GPU).
- **Master Node**: Determines which worker node meets job criteria and deploys the job.
- **Kubernetes Pod**: A group of containers run as an application on a worker node.

### Primary Components in Kubernetes
- **Node**: A server with defined resources (CPU, memory, GPU) that Kubernetes can use.
- **Cluster**: A collection of one or more nodes running containerized workloads.
- **Namespace**: An isolated environment intended for multi-tenancy, where resources must be unique and can be allocated a resource quota.
- **Container**: A self-contained runtime with the necessary dependencies, created from fixed images, existing only while being run.
- **Pod**: A group of one or more containers controlled as a single application, encapsulating application containers, storage resources, and a unique network ID.
- **Persistent Volumes**: Storage mounted on all containers in a pod, preserving data on container restarts. Pods can have multiple volumes, which exist outside the pod's scope.
- **Services**: Handle networking tasks like deploying pods, creating replicas, and deploying copies of pods as necessary.

### NVIDIA GPU Operator
The NVIDIA GPU Operator is an open-source software that automates the deployment and management of all NVIDIA software required to use GPUs on Kubernetes. It includes the NVIDIA Data Center GPU Manager (DCGM) for managing and monitoring NVIDIA data center GPUs in cluster environments, simplifying GPU administration, improving resource reliability, automating tasks, and driving overall infrastructure efficiency.

### NVIDIA Network Operator
This tool can be installed on top of the GPU Operator to enable further GPU capabilities with Kubernetes, such as GPUDirect RDMA (Remote Direct Memory Access). The MLNX_OFED is a set of networking libraries and drivers that supports RDMA over InfiniBand and Ethernet interconnects, with the goal of installing the host networking components required to enable RDMA and GPUDirect in a Kubernetes cluster.

### NVIDIA Peer Memory Driver
A client that interacts with network drivers to provide RDMA between GPUs and host memory, working alongside the GPU operator to deploy networking software.

## MLOps
Machine learning operations (MLOps) tools are often used with Kubernetes to bring an organized, methodical discipline to AI project operation and deployment, ensuring the AI infrastructure is well-utilized. Key MLOps tasks include:
- Data preparation
- Versioning of data, models, and parameters
- Monitoring experiments and results
- Deploying models for inferencing
- Monitoring model performance

MLOps tools help improve user productivity, speed up workflows, maximize resource utilization, and allow projects to scale. NVIDIA has several MLOps partners with tools that support various MLOps capabilities.

## SLURM
SLURM is a tool used for job scheduling, created by SchedMD. It is an open-source cluster management and job scheduling system for Linux clusters that is highly scalable and fault-tolerant, requiring no kernel modifications. SLURM schedules jobs to run on a subset of cluster resources and is excellent for AI training, being closely tied to Unix and Linux systems while integrating easily with existing security mechanisms.

### Slurm System Design
There are two main components:
- **Slurm Controller**: The centralized manager that manages workloads and available resources in the cluster.
- **Compute Nodes**: Responsible for running jobs and returning results. Users send commands to the Slurm controller, which manages sending jobs to compute nodes based on resource needs.

An optional database can track accounting records. NVIDIA recommends using containers to run jobs, with tools like Enroot and Pyxis allowing container usage with the Slurm scheduler. Enroot turns containers into unprivileged sandboxes, while Pyxis integrates Enroot with Slurm to ensure containers do not have root access to compute nodes.

## Conclusion
Now that you've completed this unit, you should be able to describe the difference between orchestration and scheduling, common tools used for orchestration and scheduling, and discuss the value of MLOps tools. With this knowledge, you're prepared to take on the course completion quiz. Good luck!

# Check Your Knowledge

**Question 1**  
**What is the primary purpose of the scheduler in an AI cluster?**  

- The scheduler performs data analysis and generates reports on cluster usage.  
- The scheduler determines which servers are up or down at any given time.  
- The scheduler manages the execution of jobs submitted across the cluster’s resources.  
- The scheduler optimizes the performance of individual jobs vs cluster efficiency.  

**Answer:**  
- The scheduler manages the execution of jobs submitted across the cluster’s resources.  

---

**Question 2**  
**What is the value of MLOps tools when used in conjunction with an orchestration tool like Kubernetes?**  

- MLOps tools maximize the utilization of resources and help projects to scale.  
- MLOps tools increase the amount of code created by the development team.  
- MLOps tools eliminate the need for expertise when doing an AI project.  
- MLOps tools are required for project teams to use GPUs in large AI clusters.  

**Answer:**  
- MLOps tools maximize the utilization of resources and help projects to scale.  

---

**Question 3**  
**Which of the following is included with the NVIDIA Network Operator?**  

- NVIDIA MLNX_OFED driver  
- NVIDIA GPU Operator helm charts  
- NVIDIA Kubernetes MIG Manager Distribution  
- Remote Direct Memory Access SDKs  

**Answer:**  
- NVIDIA MLNX_OFED driver