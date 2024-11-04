# GPUs and CPUs for AI

Now, let's start by reviewing GPUs and CPUs that power AI workloads in the data center. As we've already seen in earlier units, both CPUs and GPUs are components of a system that work in tandem to process code and data. 

While CPUs are designed for complex instruction sets and have evolved to include multiple cores for increased performance, GPUs are designed for simple instruction sets and have a larger number of cores for simultaneous processing. Together, they provide a powerful combination for executing code and manipulating data. 

There are different GPU and CPU architectures for different workloads. Let's explore some of those.

---

## GPU Architecture

GPU architecture is everything that gives GPUs their functionality and unique capabilities. It includes the core computational units, memory, caches, rendering pipelines, and interconnects. GPU architecture has evolved over time, improving and expanding the functionality and efficiency of GPUs.

### Latest NVIDIA Processor Architectures

Let's review some of the latest NVIDIA processor architectures, starting with GPUs:

- **Blackwell GPU Architecture**: 
  - The latest generation of accelerated computing.
  - Breaks barriers in generative AI with unparalleled performance.
  - Built to handle large-scale generative AI workflows and accelerate inference and training for the world's largest language models.

- **Hopper GPU Architecture**: 
  - Sets a new standard in accelerating large-scale AI, HPC, and data analytics.
  - Accelerates thousands of applications, such as conversational AI and language processing.
  
- **Multi-Instance GPU Support**: 
  - Both the Blackwell and Hopper GPUs support multi-instance GPU, allowing each GPU to be partitioned into as many as seven instances, each fully isolated with its own high-bandwidth memory, cache, and compute cores.

- **Ada Lovelace GPU Architecture**: 
  - Designed to provide revolutionary performance for gaming, AI-powered graphics, and ray tracing to realistically simulate the lighting of a scene.

### Grace Specialized CPU Architecture

- **Grace CPUs**: 
  - Designed for high-performance computing and data centers.
  - Provide exceptional AI and high-performance computing capabilities by combining Arm's CPU architecture with NVIDIA's expertise in AI and parallel computing.

---

## NVIDIA B200 GPU

- Based on the Blackwell architecture, the B200 GPU includes a second-generation transformer engine built to deliver the power and performance needed by transformer-based models, the backbone of many modern generative AI applications.
- The second-generation transformer engine uses custom Blackwell tensor core technology combined with NVIDIA TensorRT-LLM and NeMo framework innovations to accelerate inference and training for large language models and mixture of experts models.
- Built with 208 billion transistors and high-bandwidth memory, the B200 GPU is the world's largest and most powerful accelerator, delivering unprecedented performance, scalability, and security for any and every data center.
- The B200 also includes NVIDIA Confidential Computing, which protects sensitive data and AI models from unauthorized access without compromising performance.
- The B200 GPU has a fifth generation of NVIDIA NVLink Interconnect that can scale up to 576 GPUs to unleash accelerated performance for trillion and multi-trillion parameter AI models.
- Thanks to its decompression engine and ability to access massive amounts of memory in the NVIDIA Grace CPU, the B200 GPU can accelerate the full pipeline of database queries for the highest performance in data analytics and data science.
- Additionally, the B200 GPU includes intelligent resiliency with a dedicated reliability, availability, and serviceability engine to identify potential faults that may occur early on to minimize downtime.

---

## Historical Context

The NVIDIA Blackwell architecture was named after David Blackwell to honor his contributions to mathematics and to symbolize the architecture's capacity to drive cutting-edge computational tasks. 

- **David Blackwell**: An American mathematician and statistician known for many contributions and advancements in probability theory, game theory, statistics, and information theory. He was known for independently developing dynamic programming, as well as the Rao-Blackwell theorem used in statistics.

---

## H100 GPU

- The H100 GPU is our prior generation flagship GPU based on the Hopper architecture. It includes a transformer engine designed to speed up large language models and with 80 billion transistors, it delivers exceptional compute performance.
- The H100 has built-in confidential computing, a security approach that enables the processing of sensitive data in an encrypted and isolated environment. It addresses security concerns related to data privacy and protection, particularly in cloud computing environments.
- In addition, the H100 GPU has a scalable interconnect with 900 gigabytes per second GPU-to-GPU connectivity, enabling acceleration for the largest AI models.
- The H100 GPU also supports multiple fully isolated and secured instances, or multi-instance GPU, which allows multiple users or applications to share the same GPU while maintaining data privacy and security. 
- The H100 GPU is ideal for many applications, including training neural networks for self-driving cars.

### Naming Context

Curious why it was named Hopper? The Hopper architecture was named in honor of **Grace Hopper**, a pioneering US computer scientist. 

- **Grace Hopper**: One of the first programmers of the Harvard Mark I computer and invented one of the first linkers. Her work laid the foundation for many advancements in computer science, and her legacy continues to inspire future generations.

---

## L40S GPU

- The L40S GPU, based on the Ada Lovelace architecture, is built to power the next generation of data center workloads, from generative AI and large language model inference and training to 3D graphics, rendering, and video.
- It delivers accelerated AI performance with fourth-generation tensor cores, which are specialized hardware units found in NVIDIA GPUs. 
- Tensor cores provide groundbreaking performance for deep learning neural network training and inference functions that occur at the edge. 
- Advanced video acceleration is also a key feature of the Ada Lovelace architecture, which delivers scalability and security, providing up to twice the power efficiency of the previous generation.

### Tribute to Ada Lovelace

By naming this GPU architecture after **Ada Lovelace**, NVIDIA pays tribute to the legacy of another inspiring woman in science and mathematics.

- **Ada Lovelace**: A visionary mathematician and writer known for her pioneering work on Charles Babbage's analytical engine. Her notes and insights, published in the mid-19th century, are considered the first computer program and foretold the concept of general-purpose computing. Her contributions to the field of computing have earned her recognition as the first computer programmer and a lasting legacy in the history of technology.

---

## NVIDIA Grace CPU

- The NVIDIA Grace CPU is the first CPU designed by NVIDIA for the data center. It is built on Arm architecture and designed specifically for high-performance computing applications.
- In addition to HPC, the Grace CPU is also ideal for use in cloud computing and hyperscale data centers. Its energy efficiency and scalability make it well-suited for these environments, where large numbers of CPUs are used to power demanding workloads.
- The Grace CPU is also a good fit for applications that require large amounts of memory and high bandwidth, such as genomics, computational fluid dynamics, and quantum chemistry. These applications often involve processing large datasets and performing complex calculations, making the Grace CPU's support for large amounts of memory and bandwidth a key advantage.

### Grace CPU Superchips

The Grace CPU architecture is the foundation of three separate superchips:

1. **NVIDIA Grace Hopper Superchip**: 
   - Combines the Grace CPU with the powerful H100 GPU, making it the most versatile compute platform for scale-out.
   - Supports high-bandwidth coherent data transfers between the GPU and CPU, yielding a large unified memory model for accelerated AI and high-performance computing or HPC applications.
   - Excels when CPU performance and memory bandwidth are critical for applications such as recommender systems, graph databases, and scientific computing.

2. **NVIDIA Grace Blackwell Superchip**: 
   - Connects the NVIDIA Grace CPU with two high-performance NVIDIA B200 GPUs, using the NVIDIA NVLink Chip-to-Chip Interconnect.
   - Delivers 900 gigabytes per second of bidirectional bandwidth, allowing applications to have coherent access to a unified memory space, simplifying programming and supporting the larger memory needs of trillion-parameter LLMs and generative models for 3D data.

3. **NVIDIA Grace CPU Superchip**: 
   - Designed for CPU-based applications where absolute performance, energy efficiency, and data center density matter, such as scientific computing, cloud, data analytics, enterprise, and hyperscale computing applications.
   - Represents a revolution in compute platform design by integrating the performance level offered by a flagship x86-64 two-socket workstation or server platform into a single superchip.

---

The Grace CPU is designed for a new type of data center, one that processes mountains of data to produce intelligence. Blackwell, Hopper, and Ada Lovelace are NVIDIA's latest GPUs, excelling in diverse workloads and showcasing NVIDIA's cutting-edge technology. Known for adaptability and high performance, they provide computing for the largest workloads, such as generative AI, natural language processing, and deep learning recommendation models.

---

# Check Your Knowledge

**Question 1**  
**Which sentence best describes NVIDIA GPUs?**

- CPUs and GPUs cannot be combined on the same card.
- GPUs and CPUs can be used interchangeably to power AI applications.
- NVIDIA offers different GPU architectures for different types of workloads.
- The same GPU that powers gaming applications can be used in training large Generative AI models.

**Answer:** NVIDIA offers different GPU architectures for different types of workloads.