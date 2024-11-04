# Multi-GPU Systems

Now that we've covered the GPU and CPU solutions for AI data centers, let's see how to scale up with multi-GPU systems. As an AI solution scales, it's key to know how to scale solutions based on increased workload demand. 

There are two ways to scale: 

1. **Scale-Up (Multi-GPU)**: Refers to adding more GPUs to a single node to increase its computational power.
2. **Scale-Out (Multi-Node)**: Refers to adding more nodes to a system to increase its overall processing power.

### Comparison of Scaling Options

- **Multi-GPU Scaling**: 
  - Involves adding more GPUs to a single node.
  - Requires a node with multiple GPUs and a high-speed interconnect to allow communication between the GPUs.
  - Involves distributing data across the GPUs for parallel processing.
  - Requires load balancing between the GPUs.
  - Failure of one GPU can affect the entire system.

- **Multi-Node Scaling**: 
  - Involves adding more nodes to a system.
  - Requires multiple nodes, each with its own processing capabilities connected through a network.
  - Involves distributing data across nodes for parallel processing.
  - Requires load balancing between the nodes.
  - Provides better failure tolerance compared to multi-GPU scaling, as the failure of one node does not affect the overall system.

In the following slides, we will cover the scale-up option or multi-GPU.

---

## Multi-GPU System Implementations

As AI solutions become more complex, there is exceptional growth in computing capacity. To meet this challenge, developers have turned to multi-GPU system implementations. 

One of the keys to continued performance scaling in multi-GPU systems is flexible, high-bandwidth communication between GPUs in the system. In traditional servers, this is accomplished by using PCIe. However, as workloads continue to grow and GPUs are able to churn through data faster, the bandwidth provided by PCIe has proven to be a bottleneck. 

To address the challenge of communication between GPUs, NVIDIA introduced **NVLink** chip-to-chip interconnect to connect multiple GPUs at speeds significantly faster than PCIe offers, allowing GPUs to communicate and share memory at incredibly high speeds. However, in all-to-all communications where all GPUs need to communicate with one another, this implementation requires certain GPU pairs to communicate over a much slower PCIe data path.

To take GPU server performance to the next level and scale beyond eight GPUs in a single server, a more advanced solution was needed. With AI and HPC workloads, there are many common operations that require one GPU to talk to all the other GPUs in the system, such as distributing data to the other GPUs. Often, this happens on all GPUs simultaneously, leading to many so-called all-to-all operations.

### NVIDIA NVSwitch Technology

NVIDIA NVSwitch technology enables direct communication between any GPU pair without bottlenecks. Each GPU uses NVLink interconnects to communicate with all NVSwitch fabrics, providing the maximum amount of bandwidth to communicate across GPUs over the links.

Each **DGX H100 system** has 8 H100 GPUs. NVIDIA NVSwitch provides high bandwidth inner GPU communication. The system is configured with ten NVIDIA ConnectX-7 network interfaces, each with a bandwidth of 400 gigabits per second, providing up to 1 terabyte per second of peak bi-directional network bandwidth. 

When a system is configured with two Intel Xeon Platinum 8480C processors, it has a total of 112 cores, which means it can handle a large number of simultaneous tasks and computations. The **DGX H100** has 2 terabytes of system memory, allowing it to store and process large amounts of data. Additionally, the DGX H100 is configured with 30 terabytes of NVMe SSD storage, which can be used to store and access data quickly.

### Performance Metrics

- AI performance: 32 quadrillion floating point operations per second.

NVIDIA DGX systems are shipped pre-installed with **DGX OS** to provide a turnkey solution for running AI and analytics workloads. DGX OS offers a customized installation of Ubuntu Linux with system-specific optimizations and configurations, additional drivers, and diagnostic and monitoring tools. It provides a stable, fully tested, and supported OS to run AI, machine learning, and analytics applications on DGX supercomputers.

---

## Physical Specifications of the DGX H100 System

- **Form Factor**: 
  - An eight rack unit high chassis that fits in a standard 19-inch rack.
  - Requires a mechanical lift to help get it out of the packaging and safely installed in a rack.

- **Construction**: 
  - The DGX H100 is physically constructed from a handful of modules, each handling discrete functions in the system.
  - The front features the gold bezel familiar to anyone who has seen a DGX before.
  - Behind the bezel are the 12 dual fan modules.
  - Below those are the eight U2 NVMe drives used as a data cache, and the front console board with VGA and USB ports to connect a crash cart.
  - The front cage includes a power distribution board that connects the system to the power supplies shown at the rear of the system.
  - The front cage also holds a mid-plane, which handles communication between the motherboard tray, the GPU tray, and the components at the front of the system.

- **GPU Connectivity**: 
  - The DGX H100 system offers impressive GPU-to-GPU connectivity thanks to the presence of four fourth-generation NVLink switches, enabling high-speed data transfer and parallel processing capabilities among the installed GPUs.

- **Tray Configuration**: 
  - The GPU tray is located at the top rear of the system, with the motherboard tray underneath. The chassis holds everything together in a nice modular package.

---

## NVIDIA DGX B200 System

The **NVIDIA DGX B200** system is the latest addition to the NVIDIA DGX platform. This unified AI platform defines the next chapter of generative AI. 

- Equipped with 8 NVIDIA Blackwell GPUs interconnected with fifth-generation NVIDIA NVLink, it delivers breakthrough performance for the world's most complex AI problems, such as large language models and natural language processing.
  
- **Specifications**: 
  - **GPU Memory**: 1.4TB
  - **Processors**: Dual Intel Xeon Platinum 8570 processors
  - **System Memory**: 2TB
  - **Training Performance**: 72 petaflops FP8
  - **Inference Performance**: 144 petaflops FP4

The **NVIDIA GB200 NVL 72** is a multi-node, liquid-cooled rack-scale system for the most compute-intensive workloads. It combines 36 Grace CPUs and 72 Blackwell GPUs interconnected by fifth-generation NVLink. 

- With its liquid-cooled racks, the GB200 NVL 72 reduces a data center's energy consumption while increasing its compute density. 
- The combination of 72 NVLink-connected Blackwell GPUs with a large unified memory over a 130 TB/s compute fabric creates an exaflop AI supercomputer in a single rack.
- As a result, the NVIDIA GB200 NVL72 delivers trillion-parameter LLM training and real-time inference.

# Check Your Knowledge

**Question 1**  
**Select one correct statement about the differences between infrastructure scaling-up and scaling-out.**

- Scaling-up refers to adding more GPUs to a single node to increase its computational power, whereas scaling-out refers to adding more nodes to a system to increase its overall processing power.
- Load balancing is not a concern when scaling-up, as each GPU independently manages its workload without the need for coordination.
- When scaling-out, data is centralized on a master node for sequential processing, whereas when scaling-up each GPU processes separate sets of data independently.
- Scaling-up makes an infrastructure more resilient to failures than scaling-out.

**Answer:** Scaling-up refers to adding more GPUs to a single node to increase its computational power, whereas scaling-out refers to adding more nodes to a system to increase its overall processing power.