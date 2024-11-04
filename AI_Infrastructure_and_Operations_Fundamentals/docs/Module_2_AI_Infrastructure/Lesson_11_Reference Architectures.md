# Reference Architectures

## Outline
In this unit we will cover:
- Reference Architecture Overview
- DGX BasePOD Reference Architecture
- DGX SuperPOD Reference Architecture

## Objectives
By the end of this unit, you will be able to:
- Explain the value of reference architectures
- Desribe the information found in reference architectures
- Identify available NVIDIA reference architectures
- Desrcibe the components in the NVIDIA BasePOD reference architecture


## Unit 11: NVIDIA Reference Architectures

Welcome to unit 11, where we'll be covering NVIDIA reference architectures. 

### Unit Overview
In this unit, we will:
- Provide an overview of some reference architectures and their benefits.
- Use the DGX BasePOD reference architecture to illustrate the type of information that can be found in a reference architecture.
- Briefly look at the DGX SuperPOD and some additional reference architectures.

By the end of this unit, you should be able to:
- Explain the value of reference architectures.
- Describe the information found in reference architectures.
- Identify available NVIDIA reference architectures.
- Describe the components in the NVIDIA BasePOD reference architecture.

### Overview of Reference Architectures
Dense computing environments include many components, including:
- Multiple servers for compute
- Networking fabrics that connect the systems
- Storage for data
- Management servers

Designing systems to achieve maximum performance can be very challenging. Reference architectures are documents that present a recommended design for the implementation of a system. They utilize best-of-breed designs to provide high-performance solutions. NVIDIA has several reference architectures for datacenter-scale computing environments, including the DGX BasePOD and the DGX SuperPOD.

Reference architectures are design documents based on best practices and design principles to maximize system performance. They can serve as a foundation for building designs using various systems and components.

### Benefits of Reference Architectures
Some of the benefits of using a reference architecture include:
- Demonstrating how a specific design can help solve problems.
- Providing a foundational design that can be tailored to meet an organization's needs.
- Reducing costs and time for design and planning, which can lead to a faster solution.
- Improving quality and reliability by reducing complexity.

### NVIDIA DGX BasePOD Reference Architecture
Let’s review the reference architecture for the NVIDIA DGX BasePOD. We will explore the detailed information provided in this reference architecture, including the components in a DGX BasePOD and the various configurations available.

The NVIDIA DGX BasePOD provides the underlying infrastructure and software to accelerate the deployment and execution of AI workloads. It is an integrated solution consisting of:
- NVIDIA DGX systems
- NVIDIA networking systems
- NVIDIA Base Command software
- NVIDIA AI Enterprise software
- Partner Storage

Its reference architecture defines the components and connections needed to create a DGX BasePOD with up to 16 DGX B200 or H100 systems. It covers various configurations for a DGX BasePOD. The reference architecture document can be accessed via the provided link.

With DGX BasePOD, we’ve combined proven NVIDIA networking products, leading DGX systems for compute, storage solutions from trusted NVIDIA partners, and NVIDIA Base Command to create a cohesive, full-stack solution. Combined with NVIDIA AI, enterprise, and MLOps offerings, this setup integrates world-leading components into a streamlined system.

### Components of the DGX BasePOD Reference Architecture
The DGX BasePOD reference architecture provides overviews of:
- **DGX B200 System**: Includes eight NVIDIA B200 GPUs and can deliver 72 petaflops FP8 training performance and 144 petaflops FP4 inference performance, making it well-suited for any enterprise AI workload.
- **DGX H100 System**: Includes eight NVIDIA H100 GPUs and has a performance of 32 petaflops FP8, making it an excellent all-around system for AI development.

Both DGX systems have a 1 gigabit Ethernet port for out-of-band management through the baseboard management controller, allowing for remote management even when the system is powered off.

#### Networking Components
The next component covered in the NVIDIA DGX BasePOD reference architecture is the ConnectX-7 network adapter, which can be configured for InfiniBand or Ethernet connections. Typically, InfiniBand connections are used for the compute network, while Ethernet is utilized for storage, in-band management, and out-of-band management networks.

The DGX BasePOD reference architecture also includes an overview of NVIDIA switches that can be employed in DGX BasePOD configurations:
- **QM9700 and QM8700 InfiniBand Switches**: The QM9700 NDR InfiniBand switch with 400 gigabits per second is used with the DGX H100 system (NDR stands for Next Data Rate).
- **SN5600 Ethernet Switch**: Used for GPU-to-GPU fabrics, offering speeds between 10 gigabits Ethernet and 800 gigabits Ethernet.
- **SN4600 Switch**: Used for in-band management and can also serve as a storage fabric, with speeds ranging from 1 gigabit Ethernet to 200 gigabits Ethernet.
- **SN2201 Ethernet Switch**: Used for out-of-band management connections in the BasePOD configuration, with speeds between 1 gigabit Ethernet and 100 gigabits Ethernet.

The final configuration in the reference architecture is the DGX H100 BasePOD with NDR 200 gigabits per second InfiniBand connectivity for the compute network using QM9700 switches. This configuration utilizes ConnectX-7 network adapters for connections. The storage and management network operates on an Ethernet network using SN4600 switches. This design supports 2 to 16 DGX H100 systems. The same DGX BasePOD reference architecture can also be applied to DGX B200 systems.

### DGX SuperPOD and Additional Reference Architectures
Now, let’s take a high-level look at the DGX SuperPOD and some additional reference architectures. 

The NVIDIA DGX SuperPOD is the next-generation artificial intelligence supercomputing infrastructure based on either the DGX B200 system or the DGX H100 system. The reference architecture design introduces compute building blocks called scalable units (SU), enabling the modular deployment of a full 127-node SuperPOD with DGX B200 or H100 systems. 

The DGX SuperPOD design includes:
- NVIDIA networking switches
- Software storage
- NVIDIA AI Enterprise: a fully supported software suite optimized to streamline AI development and deployment.

A DGX SuperPOD with InfiniBand networking is recommended for enabling data scientists to train large language models like GPT-4. The DGX SuperPOD reference architecture has been deployed at customer data centers and cloud service providers worldwide.

NVIDIA also has reference architectures that are not based on specific NVIDIA servers. Some examples include:
- NVIDIA AI Enterprise reference architecture
- Cloudera Data Platform reference architecture

These reference architectures include node configurations in addition to network topology, deployment topology, and other resources to optimize design efficiency.

### Conclusion
Now that you've completed this unit, you should be able to:
- Explain the value of reference architectures.
- Describe the information found in reference architectures.
- Identify available NVIDIA reference architectures.
- Describe the components in the NVIDIA BasePOD reference architecture.

Don’t stop here—continue your learning journey with Unit 12: AI in the Cloud. See you in the next unit!

# Check Your Knowledge

**Question 1**  
**For an NVIDIA DGX BasePOD with DGX H100 systems and QM9700 switches at 200 Gbps, the number of nodes allowed is between 2 and what maximum?**

- 20 nodes
- 32 nodes
- 16 nodes
- 40 nodes

**Answer:** 32 nodes

---

**Question 2**  
**Which is an advantage of using Reference Architectures to design systems for AI workloads?**

- They are used exclusively by NVIDIA, so partners need to design their own systems.
- They focus mainly on the storage components, and the organizations are responsible for other components, such as networking and compute.
- They provide a blueprint for designing systems specific to the Financial Services industry.
- They provide a proven approach to design reliable, resilient, and robust systems.

**Answer:** They provide a proven approach to design reliable, resilient, and robust systems.

---

**Question 3**  
**Which components are part of the NVIDIA BasePOD reference architecture?**  
*(Select 2)*  

- NVIDIA L40S GPU
- NVIDIA Inference Microservices
- NVIDIA QM9700 switch
- NVIDIA DGX H100 system
- NVIDIA GB200 Superchip

**Answers:**  
- NVIDIA QM9700 switch  
- NVIDIA DGX H100 system