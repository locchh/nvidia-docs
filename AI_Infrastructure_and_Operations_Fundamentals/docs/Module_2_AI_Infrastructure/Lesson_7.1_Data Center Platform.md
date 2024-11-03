# Data Center Platform

## Outline
In this unit we will cover:
- Data Center Platform
- GPUs and CPUs fro AI Data Centers
- Multi-GPU Systems
- Introducing DPUs
- NVIDIA-Certified Systems

## Objectives
By the end of this unit, you will be able to:
- Indicate the key components and features of the NVIDIA data center platform
- Identify the GPU and CPU requirements for AI data centers, the different products available and their intented use cases
- Understand the purpose and capabilities of multi-GPU systems
- Describe the multi-node GPU interconnect technology
- Determine the role of DPUs and DOCA in an AI data center

---

## Topics Covered in This Unit
- Data center platform
- GPUs and CPUs for AI data centers
- Multi-GPU systems
- Introducing DPUs
- NVIDIA-certified systems

## Learning Objectives
By the end of this unit, you will be able to:
- Indicate the key components and features of the NVIDIA data center platform.
- Identify the GPU and CPU requirements for AI data centers, the different products available, and their intended use cases.
- Understand the purpose and capabilities of multi-GPU systems.
- Describe the multi-node GPU interconnect technology.
- Determine the role of DPUs and DOCA in an AI data center.
- Evaluate the benefits of using NVIDIA-certified systems.

---

Let's get started. First, we'll present the NVIDIA data center platform and review some considerations and requirements for building compute platforms for AI.

Modern data centers are key to solving some of the world's most important scientific, industrial, and big data challenges using high-performance computing and AI. Accelerated computing is often referred to as a full-stack challenge because it involves optimizing and integrating various components across multiple layers of the technology stack to achieve optimal performance for specialized workloads.

Furthermore, accelerated computing represents a data center scale issue, as the modern data center essentially serves as the computer. Applications span the entire data center, making it crucial to optimize all the diverse components within it.

At the foundation are the hardware technologies: GPUs, CPUs, and DPUs that form the basis for building servers. Sitting atop these servers is the software stack, encompassing CUDA and DOCA, the programming models for GPUs and DPUs respectively, along with numerous software libraries that transparently provide acceleration to developers across different hardware products, such as CUDA-X for GPU acceleration.

In addition, we offer application frameworks tailored for common domains. Some examples include:
- Riva for conversational AI
- DRIVE for autonomous vehicles
- Merlin for recommendation systems
- Many others

Customers leverage our comprehensive stack to develop and run their applications effectively. As mentioned earlier, the data center is now the new unit of computing, and to make this model work, it requires three pillars: the CPU, the GPU, and the DPU.

The GPU is used for accelerated computing, performing parallel processing at the enormous scale required for graphics and AI. The CPU continues to perform general application processing, especially basic single-thread applications, which it excels at. The DPU handles data-intensive functions like communications processing, compression, and encryption to keep the data center running efficiently. The combination of the GPU, the DPU, and the CPU is now the new unit of computing.

We'll talk about each of these in more detail in the following slides.

---

## Accelerated Systems
An accelerated system is the next phase in the evolution of computers. Just like how all smartphones today have processors for graphics and AI, every server and workstation will also have compute accelerators to power today's modern applications, including AI, visualization, and autonomous machines.

Many of these systems will also have data processing units, which accelerate the network, storage, and security services that are central to cloud-native and cloud computing frameworks. Leveraging cloud service providers (CSPs) grants customers access to computing infrastructure and resources without the need for management and maintenance. We will delve into cloud-based solutions in greater detail in a later unit.

Additionally, OEM systems are readily accessible. NVIDIA collaborates with numerous reputable, established, and certified vendors, offering flexibility in adopting solutions built from readily available components. Lastly, the NVIDIA DGX systems are purpose-built with optimized components, including networking, storage, and compute. Customers who opt for DGX solutions gain access to NVIDIA's expertise, which can assist them in deploying and maintaining their solutions effectively.

---

## AI Application Workflow
As organizations seek to build an AI application, they follow a workflow that begins with ideation and is ultimately realized as a trained model running in a production setting. The process to go from an initial concept to a production application involves several phases enacted by a team that includes data scientists, data engineers, business analysts, DevOps, and potential application developers working in concert.

The workflow shown here is an idealized example to showcase the key phases of this development process. With cloud-based GPU solutions, enterprises can access high-density computing resources and powerful virtual workstations at any time from anywhere, eliminating the need to build a physical data center. From virtual desktops, applications, and workstations to optimized containers in the cloud, data scientists, researchers, and developers can power GPU-accelerated AI and data analytics at their desks.

GPU-accelerated data centers deliver breakthrough performance for compute and graphics workloads at any scale with fewer servers, resulting in faster insights and dramatically lower costs. Sensitive data can be stored, processed, and analyzed while maintaining operational security.

---

## AI at the Edge
AI at the edge needs a scalable, accelerated platform that can drive decisions in real-time and allow every industry to deliver automated intelligence to the point of action—stores, manufacturing, hospitals, and smart cities. Jetson is the NVIDIA platform designed for edge deployments.

---

# Check Your Knowledge