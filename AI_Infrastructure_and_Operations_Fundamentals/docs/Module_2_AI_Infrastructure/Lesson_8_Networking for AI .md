# Networking for AI

## Outline
In this unit, we will cover:
- AI Data Center Networks
- Networking Requirements for AI Workloads
- InfiniBand for AI Workloads
- Ethernet for AI Workloads
- NVIDIA Networking Portfolio

## Objectives
By the end of this unit, you will be able to:
- Explain the basics of AI Data Center Networks
- Outline the networking requirements essential for AI data centers
- Summarize the main features of InfiniBand and Ethernet networking technologies employed in AI data centers
- Provide an overview of the NVIDIA networking portfolio

---

Welcome to Unit 8. Our journey of data center infrastructure leads us into the domain of AI networking. 

In this unit, we will begin with an overview of AI data center networks. Next, we will discuss the networking requirements for AI workloads. Following that, we'll delve into the networking technologies that can fulfill these requirements, including InfiniBand and Ethernet. To wrap up the unit, we'll provide an overview of the NVIDIA networking portfolio.

Let's get started.

### Overview of AI Data Center Networks
A typical AI data center will have four networks:

1. **Compute Network**: 
   - Designed to minimize system bottlenecks and maximize performance for the diverse nature of AI workloads.
   - Provides redundancy in the event of hardware failures and minimizes costs.

2. **Storage Network**: 
   - Provides high throughput access to shared storage.
   - High bandwidth requirements with advanced fabric management features provide significant benefits for the storage fabric.

3. **In-Band Management Network**: 
   - Provides connectivity to the management nodes.
   - Primary network for everything that isn't interjob communication or high-speed storage access (e.g., cluster management services, SSH, DNS, job scheduling, access to the NFS home file system, external services).

4. **Out-of-Band Management Network**: 
   - Provides remote management functions, even if servers are offline or unreachable on the in-band network.
   - Ensures management traffic does not interfere with other cluster services or user jobs.

### Networking Requirements for AI Workloads
GPUs process data quickly and in parallel. To get the greatest efficiency from GPU-based systems, GPU utilization must remain as high as possible. This means that GPUs will need high bandwidth transfers for large quantities of data. As AI continues to advance, the models and related datasets are growing, requiring large amounts of data to be stored and passed to the compute system.

Many AI models must be run across multiple GPU nodes, necessitating data transfers to and from GPUs. Given these complexities, it's evident that the performance of AI models on GPU-based systems depends not solely on hardware, but on the interplay of data management, GPU utilization, and network configurations.

Key networking factors that influence performance include:
- **Network Topology**
- **Bandwidth and Latency**
- **Network Protocols**
- **Data Transferring Techniques**
- **Management Methods**

### Differences Between Traditional and AI-Optimized Networks
A traditional network optimized for cloud operates differently from a network optimized for AI data centers:

- **Traditional North-South Network**:
  - Runs storage, controls traffic, and is a legacy network.

- **AI-Optimized Network**:
  - Connects GPU to GPU with high-speed storage, is lossless for RDMA operations, and has low latency.

Legacy networks run TCP, while AI-optimized networks run RDMA. Legacy networks can operate with high jitter, while AI-optimized networks must avoid jitter.

The applications running on these infrastructures differ as well. Traditional cloud applications run independently, whereas AI data centers have dependencies between nodes. The slowest element in the fabric sets the speed for the entire AI cluster.

### AI Supercomputers
NVIDIA AI supercomputers are increasingly used in two settings: **AI factories** and **AI clouds**.

- **AI Factories**:
  - Used for the largest AI training tasks and require high computational horsepower.
  - Built to train and refine large, complex foundational AI models at scale.

- **AI Clouds**:
  - Serve multiple users and run smaller, less complex jobs.
  - Initially supported by Ethernet, but demands have grown due to the need for reliable support for larger workloads, such as generative AI.

### InfiniBand Protocol
InfiniBand is a networking technology designed to deliver high throughput and low latency while minimizing processing overhead. 

- Maintained by the InfiniBand Trade Association (IBTA), it provides a solution from the hardware layer to the application layer.
- Allows high-speed connections between compute systems and storage.
- Features include remote direct memory access (RDMA), which enables devices to access memory directly without CPU intervention.

InfiniBand is favored in traditional HPC and is deployed in large-scale machine learning systems for training and inference.

### Ethernet Protocol
Ethernet, standardized in the 1980s, is the predominant LAN technology. 

- It supports various applications, from home networks to corporate LANs to data center interconnects.
- Throughput has evolved from 10 Mbps to 400 Gbps, with a focus on compatibility across applications.

**RDMA over Converged Ethernet (RoCE)** allows RDMA over Ethernet networks, enhancing interoperability and performance for AI, storage, and big data applications.

### GPUDirect RDMA
GPUDirect RDMA provides direct communication between NVIDIA GPUs in remote systems, minimizing CPU utilization and the required buffer copies of data via system memory.

- Simplifies the packet flow process by allowing packets to be sent directly to the GPU for processing.

### Overview of the NVIDIA Networking Portfolio
Growing AI workloads increase the demand for more computing power, efficiency, and scalability. NVIDIA provides complete end-to-end solutions supporting InfiniBand and Ethernet networking technologies:

- **NVIDIA ConnectX**: Advanced hardware offloads and accelerations for AI workloads.
- **NVIDIA BlueField DPUs**: Provide a secure and accelerated infrastructure.
- **NVIDIA Spectrum Ethernet Switch Family**: Delivers performance, scalability, and reliability across applications.
- **NVIDIA Quantum InfiniBand Switch Family**: Offers high performance for data center operations.
- **NVIDIA LinkX Product Family**: A comprehensive line of interconnect products.

### Spectrum-X Networking Platform
The NVIDIA Spectrum-X networking platform is designed specifically to enhance Ethernet performance in AI clouds.

- Achieves 1.6 times effective bandwidth for AI workloads, increasing AI performance and energy efficiency.
- Combines Spectrum-4 Ethernet switch and BlueField-3 DPUs to minimize congestion and latency while improving bandwidth.
- Spectrum-X uses standards-based Ethernet and is interoperable with any Ethernet-compatible device.

### Conclusion
Now that you have completed this unit, you should be able to explain the basics of AI data center networks, outline the networking requirements essential for AI data centers, summarize the main features of InfiniBand and Ethernet networking technologies, and provide an overview of the NVIDIA networking portfolio.

Continue the learning journey with Unit 9, **Storage for AI**. See you in the next unit!

# Check Your Knowledge

**Question 1**  
**What is a key difference between a legacy network and an AI-optimized network?**

- Legacy networks run TCP while AI-optimized networks run RDMA.
- Legacy networks run RDMA while AI-optimized networks run TCP.
- In legacy networks, applications have high dependencies between nodes, while in AI-optimized networks, applications run independently with no dependencies.
- Legacy networks can operate with high jitter, while AI-optimized networks can operate with high latency.

**Answer:** Legacy networks run TCP while AI-optimized networks run RDMA.

---

**Question 2**  
**What is one of the key features of InfiniBand in high-performance computing?**

- Intelligent offloading for optimized data processing.
- Accelerating storage technologies and transferring data at high speeds.
- GPU-to-GPU communication at incredibly high speeds.
- Prioritizing data transmission based on computational requirements.

**Answer:** Intelligent offloading for optimized data processing.

---

**Question 3**  
**Which of the sentences below best describes RoCE (RDMA over Converged Ethernet)?**

- It encapsulates InfiniBand transport packets within Ethernet frames to enable RDMA over Ethernet networks.
- It is an NVIDIA technology allowing data transfer with minimal CPU intervention.
- It allows direct communication between GPUs in remote systems.
- It is the predominant LAN technology for AI workloads.

**Answer:** It encapsulates InfiniBand transport packets within Ethernet frames to enable RDMA over Ethernet networks.