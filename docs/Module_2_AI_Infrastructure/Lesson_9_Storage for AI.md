# Storage for AI

## Welcome to Unit 8

Our journey of data center infrastructure leads us into the domain of AI networking. In this unit, we will begin with an overview of AI data center networks. Next, we will discuss the networking requirements for AI workloads. Following that, we'll delve into the networking technologies that can fulfill these requirements, including InfiniBand and Ethernet. To wrap up the unit, we'll provide an overview of the Nvidia networking portfolio. 

By the end of this unit, you'll be able to:
- Explain the basics of AI data center networks
- Outline the networking requirements that are essential for AI data centers
- Summarize the main features of InfiniBand and Ethernet networking technologies employed in AI data centers
- Provide an overview of the Nvidia networking portfolio

Let's get started. 

### Overview of AI Data Center Networks

A typical AI data center will have four networks:
1. **Compute Network**: Designed to minimize system bottlenecks and maximize performance for the diverse nature of AI workloads. It also provides some redundancy in the event of hardware failures and minimizes costs.
  
2. **Storage Network**: Provides high throughput access to shared storage. High bandwidth requirements with advanced fabric management features provide significant benefits for the storage fabric.

3. **In-band Management Network**: Provides connectivity to the management nodes. It's the primary network for everything that isn't interjob communication or high-speed storage access, such as cluster management services, for example, SSH, DNS, and job scheduling, access to the NFS home file system, and external services like the NGC registry, code repositories, or data sources.

4. **Out-of-band Management Network**: Provides remote management functions, even if servers are offline or unreachable on the in-band network. It provides remote power control, a remote serial console, and temperature and power sensors. A separate network ensures that management traffic does not interfere with other cluster services or user jobs.

### Networking Requirements for AI Workloads

GPUs process data quickly and in parallel. To get the greatest efficiency from GPU-based systems, GPU utilization must remain as high as possible. This means that GPUs will need high bandwidth transfers for such large quantities of data. As AI continues to advance, the models and related datasets are growing. Therefore, large amounts of data must be stored and passed to the compute system.

In addition to the large amount of data, many AI models must be run across multiple GPU nodes. This requires the transfer of data to and from GPUs. Given these complexities and requirements, it becomes evident that the performance of AI models on GPU-based systems is not solely dependent on the hardware. Rather, it's the interplay of data management, GPU utilization, and network configurations that truly drives performance.

Now let's delve into the key networking factors that influence this performance. There are several networking-related key factors that affect performance: network topology, bandwidth and latency, network protocols, data transferring techniques, and management methods. Some of them will be discussed in this unit.

As computing requirements continue to grow, the network is critical for maximizing the acceleration provided by the GPU. In the world of GPU computing, the transfer of input and output data to the GPU is a very expensive task in terms of time. To maximize GPU-based acceleration, data must always be available for the GPU to operate upon. Because the GPU has so many processing elements, this can become a challenge. Obviously, you wouldn't want those elements to be inactive; they want to be fed all the time.

As you would expect, several techniques are employed to optimize data movement to the GPU. Within a server, this means the CPU, memory, and storage must support bandwidth speeds and latency that do not cause significant GPU idle time.

### Traditional Networks vs. AI-Optimized Networks

What is the difference between a traditional network optimized for cloud and a network that's optimized for AI data centers? The way to think about it is that there are two different types of networks. 

- On the left is a traditional north-south network. It runs storage, controls traffic, and is a legacy network.
- On the right is a network optimized for AI. It connects GPU to GPU, may have high-speed storage, is lossless for RDMA operations, and has low latency.

The legacy network runs TCP, while the network optimized for AI runs RDMA. Legacy networks can operate with high jitter, while AI-optimized networks must avoid jitter.

There's also a difference in the applications that run on the infrastructure. When you build a traditional cloud, you have a lot of applications that all run independently, meaning they have no dependencies on each other. When you build an AI data center, it's very similar to an HPC cluster. There's a lot of dependency between all the nodes, and the slowest element in the fabric sets the speed for the entire fabric and the entire AI cluster. This element could be a slow CPU, high jitter, or high tail latency, for example.

The key measurement for the AI-optimized network is how long an AI training job takes from start to finish. 

### AI Factories and AI Clouds

Nvidia AI's supercomputers are increasingly in use around the world, generally in two settings: AI factories and AI clouds. 

- **AI Factories**: Used for the largest AI training tasks. They require tremendously high computational horsepower, and the AI supercomputers that power them are built to train and refine very large, complex, foundational AI models at extreme scale. The only way these systems can deliver such towering performance is to use a specialized network comprising NVLink and InfiniBand within network computing. AI factories typically have one tenant or user and one job or a handful of jobs working at the same time.

- **AI Clouds**: These are hyperscale systems serving volumes of users, hosting multi-tenants, and running many less complex, smaller, and lower scale jobs. The decreased demand for scale and performance of these systems are effectively served using Ethernet as their common network until now. However, the demands on AI clouds have grown in scale. Support is still needed for small scale jobs, multi-tenant, and security, but now AI clouds must occasionally provide reliable support for large workloads such as generative AI. Traditional Ethernet networks, built for general clouds or traditional data centers, are just too slow for the new generative AI workloads.

### InfiniBand for AI Workloads

In this chapter, we'll review the InfiniBand protocol and how it helps to maximize the performance of the AI data center. InfiniBand is a networking technology designed to deliver both high throughput and low latency while minimizing processing overhead. The InfiniBand specification is maintained by the InfiniBand Trade Association (IBTA) and provides a solution starting from the hardware layer and continuing to the application layer. 

InfiniBand is an interconnect technology that allows high-speed connections between compute systems and storage. In systems with multiple compute and storage nodes, a technology like InfiniBand is necessary to ensure that data transfers are high bandwidth and efficient. Apart from its low latency and high bandwidth capabilities, the InfiniBand interconnect also introduces intelligent offloading features. InfiniBand is a favorite of traditional HPC. It runs scientific simulations and models on parallel clusters as well as for cloud data centers and GPU-accelerated AI workloads. InfiniBand solutions are the most deployed high-speed interconnect for large-scale machine learning used for both training and inference systems.

One of InfiniBand's key features is remote direct memory access (RDMA). Direct memory access (DMA) is the ability of a device such as a GPU or network adapter to access host memory directly without the intervention of the CPU. RDMA extends DMA with the ability to access memory on a remote system without interrupting the processing of the CPU on that system. InfiniBand network adapters, also called host channel adapters (HCAs), include hardware offloading, allowing for faster data movement with less CPU overhead as it bypasses the TCP/IP stack altogether.

In summary, RDMA offers:
- Efficient data transfer
- OS bypass enables the fastest access to remote data possible
- Efficient computing that reduces power, cooling, and space requirements
- Support for message passing, sockets, and storage protocols
- Support by all major operating systems

### Ethernet for AI Workloads

In this chapter, we'll examine the Ethernet protocol and its role in optimizing the performance of AI data centers. Ethernet was introduced in 1979 and was first standardized in the 1980s as IEEE standards. Ethernet describes how network devices can format and transmit data to other devices on the same local area network. Ethernet has become the predominant LAN technology, thanks to its ability to evolve and deliver higher levels of performance while also maintaining backward compatibility.

Ethernet's original 10 megabits per second throughput increased to 100 megabits per second in the mid-1990s and currently supports up to 400 gigabits per second. Ethernet is designed to suit the needs of a broad range of applications, ranging from home networks to corporate LANs to data center interconnects. Naturally, each type of application has unique requirements and protocols it must support. 

InfiniBand, on the other hand, has one focus, which is to be the highest performance data center interconnect possible. InfiniBand has lower latency than Ethernet and provides optimal performance for multi-node AI training. 

**RDMA over Converged Ethernet (RoCE)** is a technology that allows RDMA over Ethernet networks. RoCE uses the InfiniBand packet header and encapsulates it with a UDP header that's carried over the Ethernet network. UDP is a very simple and flexible transport protocol that offers a great deal of interoperability and compatibility with legacy hardware. By making use of UDP encapsulation, RoCE can transcend layer 3 networks. RoCE is an open source and formal InfiniBand Trade Association standard. RoCE is becoming an important technology fundamental to accelerating AI, storage, and big data applications, even if InfiniBand's RDMA is leaner and meaner.

**GPUDirect RDMA** provides direct communication between Nvidia GPUs in remote systems.

 It provides a direct or peer-to-peer data path between the GPU memory directly to and from the Nvidia networking adapters. It minimizes CPU utilization and the required buffer copies of data via the system memory. Nvidia adapter cards have onboard processing power that can aggregate data and send smart interrupts to the CPU, utilizing near 0% of processing cycles from the CPU.

In order to understand GPUDirect RDMA, let's look at the regular packets flow first. Packets are received from a remote node by the host channel adapter. The packets are sent via the PCI bus and copied to the system memory. Packets are handled by the CPU and then copied again to the GPU memory via the PCI bus. With GPUDirect RDMA, the process is simplified. Packets are received by the host channel adapter and sent directly to the GPU for processing.

To summarize, GPUDirect RDMA:
- Saves full copy operations
- Reduces PCI transactions and CPU usage
- Improves end-to-end latency

### Nvidia Networking Portfolio

This section will provide an overview of the Nvidia networking portfolio. Growing AI workloads are increasing the demand for more computing power, efficiency, and scalability. To meet these needs, Nvidia provides complete end-to-end solutions, supporting InfiniBand and Ethernet networking technologies. 

The industry-leading Nvidia ConnectX family of super network interface cards (SuperNIC) offers advanced hardware offloads and accelerations for AI workloads. The Nvidia BlueField DPUs and BlueField SuperNICs provide a secure and accelerated infrastructure for any workload in any environment from cloud to data center to edge. A DPU is designed to offload, accelerate, and isolate infrastructure workloads.

The Nvidia Spectrum Ethernet switch family includes a broad portfolio of top-of-rack and aggregation switches, delivering industry-leading performance, scalability, and reliability across a wide range of applications. The Nvidia Quantum InfiniBand switch family, comprising fixed configuration and modular switches, provides the dramatic leap in performance needed to achieve unmatched data center performance with less cost and complexity. 

Finally, the Nvidia LinkX product family of cables and transceivers provides the industry's most complete line of interconnect products for a wide range of applications.

### Nvidia Spectrum-X Switches

Let's explore the Nvidia Spectrum-X switches specifically designed for Ethernet use within AI data centers. The Nvidia Spectrum-X networking platform is the first Ethernet platform designed specifically to improve the performance and efficiency of Ethernet-based AI clouds. This breakthrough technology achieves 1.6 times the effective bandwidth for AI workloads, increasing AI performance and energy efficiency, along with consistent predictable performance in multi-tenant environments.

Spectrum-X is a Nvidia full stack solution that leverages network innovations that only work with the combination of the Nvidia Spectrum-4 Ethernet switch and Nvidia BlueField-3 data processing units (DPUs). The combination of the Spectrum-4 Ethernet switch and Nvidia BlueField-3 DPUs installed on compute servers improves the standard Ethernet protocol by minimizing congestion and latency while improving bandwidth.

With that said, Spectrum-X uses standards-based Ethernet and is fully interoperable with any device that communicates with Ethernet. Spectrum-X is a pioneering solution designed specifically for the AI landscape. It harnesses the potent synergy of the Nvidia Spectrum-4 Ethernet switch and the Nvidia BlueField-3 DPU, ensuring unmatched performance. This platform delivers exceptional performance across AI, machine learning, natural language processing, and various industry-specific applications.

Spectrum-X empowers organizations to elevate AI cloud performance, enhance power efficiency, and achieve superior predictability and consistency. Crucially, it undergoes rigorous tuning and validation across the entire Nvidia hardware and software stack, ensuring an unparalleled Ethernet solution for AI clouds.

### Nvidia RoCE Enhancements

Nvidia's RoCE adaptive routing is a fine-grained load balancing technology that dynamically reroutes RDMA data to avoid congestion and provide optimal load balancing. It improves network utilization by selecting forwarding paths dynamically based on the state of the switch such as queue occupancy and port utilization. 

Nvidia's RoCE congestion control is a mechanism used to reduce packet drops in lossy networks or congestion spreading in lossless networks. It limits the injection rate of flows at the ports causing congestion, thereby reducing switch buffer occupancy, decreasing latency, and improving burst tolerance. Nvidia's RoCE adaptive routing and congestion control Ethernet enhancements require Spectrum-4 switch and BlueField-3 DPU to work in unison.

### Conclusion

Now that you have completed this unit, you should be able to explain the basics of AI data center networks, outline the networking requirements essential for AI data centers, summarize the main features of InfiniBand and Ethernet networking technologies employed in AI data centers, and provide an overview of the Nvidia networking portfolio.

Don't stop here. Continue the learning journey with Unit 9: Storage for AI. See you in the next unit.

## Keywords
Here are the keywords extracted from the provided text:

- Storage considerations
- AI workloads
- Storage requirements
- Storage file systems
- Nvidia validated storage partners
- Model accuracy
- Model complexity
- Image classification
- Autonomous driving
- Natural language processing
- Data storage
- Fast
- Flexible
- Scalable
- Input/output operations per second (IOPS)
- Bandwidth
- Metadata operations
- Data management
- Resiliency
- Fault tolerance
- Data lifecycle
- Network file systems
- Local storage
- Distributed file systems
- Parallel file systems
- Object storage
- SQL and NoSQL databases
- NFS (Network File System)
- POSIX (Portable Operating System Interface)
- Data replication
- REST API
- Security features
- Caching
- Training performance
- Read and write performance
- Storage hierarchy
- Multi-tiered storage
- Data accessibility
- Performance metrics
- Energy efficient computing

Let me know if you need anything else!