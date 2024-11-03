# Introduction to DPUs

Now that we have a solid understanding of GPU and CPU requirements and implementations in an AI data center, let's explore the third pillar of a data center: the **DPU**. 

DPUs are designed to meet the infrastructure requirements that modern data centers must offer for today's cloud computing and AI workloads, providing a secure and accelerated infrastructure. The best definition of the DPU's mission is to **offload, accelerate, and isolate** infrastructure workloads.

- **Offload**: DPUs take over infrastructure tasks from the server CPU, allowing more CPU power to be used for running applications. DPUs run infrastructure functions more quickly than the CPU can by using hardware acceleration in the DPU silicon, thus accelerating network traffic and improving application performance.

- **Isolate**: DPUs move critical data plane and control plane functions to a separate domain on the DPU, relieving the server CPU from work and protecting these functions in case the CPU or its software is compromised.

### Data Processing Unit (DPU)

The **Data Processing Unit**, or DPU, is a data center infrastructure on a chip that enables organizations to build software-defined hardware-accelerated IT infrastructure. Running infrastructure services on the host CPU steals precious CPU cores, which impacts application performance and reduces efficiency, sometimes severely. The role of the DPU is to offload and isolate the infrastructure services from the host CPU and accelerate them in hardware by leveraging purpose-built hardware accelerators. This frees up the host CPU for revenue-generating applications and improves data center performance, efficiency, scalability, and security.

A DPU has several specialized accelerators for networking, security, and storage. These accelerators are designed to execute these tasks much more efficiently than the CPU cores, allowing for greater amounts of data to be processed more quickly and often using significantly less power. It can also run compute-heavy tasks in environments where the physical footprint is limited, such as in far edge applications.

### NVIDIA BlueField-3 DPU

The **NVIDIA BlueField-3 Data Processing Unit** is the third generation infrastructure compute platform that enables organizations to build software-defined hardware-accelerated IT infrastructures from cloud to core data center to edge. 

- **Connectivity**: With 400 gigabits per second Ethernet or NDR 400 gigabits per second InfiniBand network connectivity, the BlueField-3 DPU offloads, accelerates, and isolates software-defined networking, storage, security, and management functions in ways that profoundly improve data center performance, efficiency, and security.

- **Functionality**: BlueField DPUs provide a secure and accelerated infrastructure by offloading, accelerating, and isolating a broad range of advanced networking, storage, and security services. From cloud to core to edge, it increases efficiency and performance.

### Use Cases for NVIDIA BlueField DPUs

The world's largest Cloud Service Providers (CSPs) have adopted DPU technology to optimize the data center infrastructure stack for incredible efficiency and scalability. BlueField is used in bare metal virtualized cloud data centers and, more recently, in Kubernetes clusters, often running on bare metal infrastructure.

- **Secure Infrastructure**: BlueField DPUs enable a secure infrastructure in bare metal clouds.

- **Cybersecurity**: BlueField is used in Next Generation Firewalls (NGFW), micro-segmentation, and various security applications, enabling a zero-trust security architecture that extends beyond the data center perimeter to the edge of every server.

- **Performance**: In HPC and AI, telco enterprise storage, and CDN (Content Delivery Networks), BlueField adds significant value in accelerated performance, new functionality, and more. By supporting NVMe Over Fabrics (NVMEOF), GPU direct storage, data integrity, decompression, and deduplication, BlueField provides high-performance storage access for remote storage that rivals direct-attached storage.

- **Video Streaming**: BlueField reduces CPU cycles in video streaming by offloading and accelerating video streaming tasks to the DPU.

### NVIDIA DOCA

**NVIDIA DOCA** is the open cloud SDK and acceleration framework for BlueField DPUs. By leveraging industry-standard APIs, DOCA unlocks data center innovation by enabling the rapid creation of applications and services for BlueField DPUs. It supports BlueField-3 and empowers thousands of developers, simplifying the development of networking, storage, and accelerating infrastructure services in the cloud.

---

Now that you have an understanding of the three pillars of the data center—GPU, CPU, and DPU—let's review the **NVIDIA-certified servers** that provide an end-to-end platform for accelerated computing.

### NVIDIA-Certified Systems

An **NVIDIA certified system** brings together NVIDIA GPUs and NVIDIA networking onto systems from leading vendors. It conforms to NVIDIA's design best practices and has passed a set of certification tests that validate the best system configurations for performance, manageability, scalability, and security.

- **Enterprise Confidence**: With NVIDIA-certified systems, enterprises can confidently choose performance-optimized hardware solutions backed by enterprise-grade support to securely and optimally run their accelerated computing workloads, both in smaller configurations and at scale.

- **Security**: NVIDIA certified servers help to secure workflows by protecting data at the platform, network, and application layers. Whether deployed in a data center or at the edge, laptops, or desktops, customers can be assured they don’t have to compromise on security features when running accelerated applications.

- **Optimized Functionality**: Certified servers bring together a comprehensive set of technologies and server configurations that have been validated for optimal functionality. Depending on the choice of GPU and network adapter, workloads can benefit from numerous capabilities for performance, security, and scalability.

- **Acceleration**: GPUs provide record-setting acceleration of many algorithms in machine learning, deep learning, and data analytics. In addition to fast video processing and rendering, high-speed interconnects allow data to be moved quickly to servers and directly to GPUs for faster processing. 

- **Security Features**: Network encryption offload for TLS and IPsec provides security for data in motion without compromising throughput, while key management and secure boot features ensure host-level security.

- **Multi-Node Processing**: Accelerated data transfer between GPUs and servers unlocks efficient multi-node processing for the largest tasks, such as large AI model training. Conversely, multi-instance GPUs allow a single GPU to be split into multiple independent GPU instances, enabling flexible utilization.

### Conclusion

Now that you've completed this unit, you should be able to:

- Indicate the key components and features of the NVIDIA data center platform.
- Identify the GPU and CPU requirements for AI data centers, the different products available, and their intended use cases.
- Understand the purpose and capabilities of multi-GPU systems.
- Describe the multi-node GPU interconnect technology.
- Determine the role of DPUs and DOCA in an AI data center.
- Evaluate the benefits of using NVIDIA-certified systems.

Continue your journey by taking the next unit: **Networking for AI**.

## Keywords
Here are the extracted keywords:

- DPU (Data Processing Unit)
- Infrastructure requirements
- Cloud computing
- AI workloads
- Offload
- Accelerate
- Isolate
- Hardware acceleration
- Data plane
- Control plane
- Software-defined infrastructure
- BlueField-3 DPU
- Ethernet connectivity
- InfiniBand
- Networking
- Storage
- Security
- Management functions
- Cloud Service Providers (CSPs)
- Bare metal infrastructure
- Kubernetes clusters
- Cybersecurity
- Next Generation Firewalls (NGFW)
- Micro-segmentation
- Zero trust security
- HPC (High-Performance Computing)
- NVMe Over Fabrics (NVMEOF)
- GPU direct storage
- Data integrity
- Decompression
- Deduplication
- Video streaming
- NVIDIA DOCA
- Open cloud SDK
- Data center innovation
- NVIDIA-certified servers
- Accelerated computing
- Performance optimization
- Manageability
- Scalability
- Security features
- Machine learning
- Deep learning
- Data analytics
- High-speed interconnects
- Network encryption offload
- TLs and IPsec
- Multi-node processing
- Multi-instance GPUs
- AI model training
- Host-level security
- Unit completion goals