# Accelerating AI with GPUs

## Welcome to the Accelerating AI Using Nvidia GPUs Unit
This unit introduces you to Nvidia GPUs, the engines for accelerated compute. Let's jump over to the agenda to see what we have in store in this unit.

## Agenda
In this unit, we cover:
- A historical perspective on GPUs, exploring why they were developed and how they've evolved to become key components in accelerating computing in modern data centers.
- A deep dive into general GPU architecture.
- A head-to-head comparison between CPUs and GPUs.
- An overview of GPU server systems within the data center.
- An introduction to the last three generations of Nvidia GPU architecture.

## Learning Objectives
After completing this unit, you should be able to:
- Recall significant milestones in GPU history and describe key developments in the evolution of GPU technology.
- Explain the core components of GPU architecture and their functions, demonstrating a clear understanding of how GPUs work.
- Analyze and compare the architectural differences between CPUs and GPUs, highlighting their strengths and limitations in various computing scenarios.
- Apply knowledge of GPU server systems to plan, configure, and deploy GPUs effectively, considering hardware configurations and deployment strategies.
- Evaluate Nvidia's AI GPU families, assess their features, and determine which GPU family best suits specific AI and deep learning use cases based on their capabilities and characteristics.

## Introduction to GPU History
Delving into the rich and ever-evolving history of GPUs, we uncover the milestones and technological transformations that have shaped the world of graphics processing. A graphics processing unit (GPU) is a specialized electronic circuit designed to rapidly manipulate and alter memory to accelerate the creation of images in a frame buffer intended for output to a display device. 

Computer graphics have undergone significant evolution since the 1970s. Their importance cannot be overstated as humans primarily rely on vision to process the information presented by computers. Images on screens are comprised of picture elements, or pixels. A pixel is the smallest unit of a digital image that can be displayed and represented on a digital display device. 

Pixel characteristics include position, color, and brightness. Every pixel in an image must be processed at such a rate that the human eye does not perceive any delays or inconsistencies as it absorbs the image being presented. As display and computer technology have advanced, screens now have more pixels, leading to more realistic image representation. This is referred to as screen resolution, which represents pixel density. 

The processing behind the pixels is done by the GPU. As screen resolutions have increased, the processing power necessary to represent each pixel has also increased. GPUs have evolved over time to become a fundamental building block in computer architecture. The 1980s saw the development of individual graphics display processors, and the 1990s saw the development of separate boards or cards that can be modularly replaced in computer systems.

## Understanding GPU Architecture
Now that you have an understanding of the history and evolution of the GPU, let's turn our attention to this groundbreaking architecture. GPU architecture forms the core foundation of modern graphics processing. In this exploration, we'll delve into the intricate design and functionality that powers these essential components of accelerated computing.

This is an image of a typical GPU. At the heart of the chip are thousands of GPU cores. A core is the component of the GPU that processes data, alongside onboard cache memory, which acts as a typical cache, storing a copy of everything for quick, reliable data access. Parallel processing is possible with the use of multiple cores. Closest to the cores is the high-speed GPU memory. This memory is designed specifically for GPU use and can be shared with other GPUs.

## The Rise of Nvidia GPU Computing
Now that you have an understanding of the general GPU architecture, let's turn our attention to the factors that have led to the rise of Nvidia GPU computing. AI models continue to grow in complexity and at an astonishing rate. In just the past three years, the size of state-of-the-art AI models has grown by three orders of magnitude, and this exponential pace will continue. 

This growth in data and AI model sizes requires more compute, which is possible through GPUs but not through CPUs. It also requires a mature set of frameworks and tools to maximize performance and accelerate deployment. Nvidia is at the center of the AI stack, from architecture and platforms to CUDA, from frameworks to the Triton server and NGC. 

GPU computing has given the industry a path forward to keep up with the expected performance evolution. This success is achieved through a highly specialized parallel processor design, which permeates the approach to system design, system software, algorithms, and optimized applications. Continuous optimizations between hardware and software produce ongoing performance gains.

## Key Data Center Trends
Let's explore some key data center trends that also contribute to the rise in GPU computing. The data center landscape is accelerating. Consider the pace at which new services are being adopted and how AI is accelerating the adoption of new services and capabilities. For instance, let's examine the time it took these apps to amass 100 million users. WhatsApp attained 100 million users in 49 months, while ChatGPT did so in just two months. 

AI is accelerating how fast new services come along and connect with the community, stimulating demand for advanced computing power. At the same time, there is sensitivity to climate change and the need for greener computing. There's also a challenge to get access to more compute in data centers around the world. 

Data center energy usage is exceeding 200 terawatts per year. The data center represents about 2% of global energy usage, and this percentage is projected to increase to 5% by 2030. Data centers are power limited and take years to plan and build. To meet the demand for delivering these new services, data center operators need to optimize the infrastructure they have within the power-constrained data centers they possess. Accelerated computing is one way to achieve that goal.

## The Future of Accelerated Computing
Let's explore why accelerated computing is the path forward. Nvidia CEO Jensen Huang famously stated, "Moore's Law is dead," making this bold claim several times dating back to 2017. The end of Moore's Law refers to the slowing down of exponential transistor density growth on microchips, leading to challenges in achieving regular and significant performance improvements in traditional semiconductor technology. 

It's essentially a physics problem, as transistors would eventually reach the limits of miniaturization. CPUs are simply unable to keep up with the complex workload demands associated with accelerated computing. This limitation will only get worse as the size and complexity of models increase. 

Accelerated computing requires a comprehensive and integrated full-stack approach that encompasses hardware, software, and frameworks to harness the full potential of accelerators like GPUs for complex workloads. For example, an NVIDIA AI platform with H100 GPUs set new time-to-train records at scale across every workload. This includes the new LLM workload, where training times were reduced from days to hours and, in the case of the largest LLMs, from a month down to a week. 

It's important to highlight that NVIDIA consistently pushes the boundaries of GPU technology, as demonstrated by our latest innovation, the Grace Hopper GH200, which we will delve into in Unit 7, focusing on compute platforms for AI.

## CPU vs. GPU Comparison
Let's perform a deep dive comparison between the CPU and GPU to better understand the strengths and weaknesses of each. In the world of computing, understanding the distinctions between CPUs and GPUs is pivotal. In this topic, we embark on a journey to compare and contrast these fundamental processing units. 

Central processing units (CPUs) are computer components designed to process complex instruction sets that execute code and manipulate data. Originally, instructions were processed one at a time in the processing unit of the chip called the core. The core reads and executes the program instructions. As CPU architecture evolved, multicore processors were developed, allowing several instructions to be processed simultaneously, leading to increased processing performance. 

GPUs are designed to execute simple instruction sets. Consequently, the number of cores that can be built in a comparatively similar silicon area is much larger than with the CPU. With relatively many more cores than a CPU, a GPU allows processing of many simple instructions simultaneously. Both CPUs and GPUs are system components that work in tandem to process code and data.

### CPU Characteristics
Over the last few years, CPUs have moved to a multi-core architecture, with the latest CPUs containing up to 128 cores with fast clock speeds. CPUs also have large main memory; however, the bandwidth of that memory is relatively low, affecting how quickly we can move data. 

CPUs are designed to run multiple different applications concurrently. Each of these applications is assigned to a single thread or a small number of threads and is scheduled in a time-sliced manner to run on the CPU. This requires low latency to minimize the delay between issuing a request for data and executing the instructions on that data. This implies large caches to hold the data required by the threads and complex control logic to ensure that the data is ready to go when the thread is running.

One consequence of this is that a large amount of the silicon on a CPU is dedicated to data movement, meaning that CPUs have relatively low performance per watt, as a significant proportion of the energy is used for data movement rather than actual calculations. In addition, there are cache misses when trying to access data that isn't in the cache yet, which can be very detrimental to performance.

### GPU Characteristics
In comparison, a GPU is optimized for executing highly parallel tasks, stemming from its roots in generating actual computer graphics, where the same operation is applied to millions of pixels multiple times a second to render scenes. Modern GPUs have a huge number of compute cores—over 10,000 for some of the latest cards. 

However, these compute cores don't have the complex logic for pre-fetching data, for example. So instead, the GPU deals with the issue of latency by hiding it with computation. Essentially, we assign the GPU more tasks than its physical cores can handle, contrasting the approach taken with the CPU. 

The GPU scheduler launches a thread that tries to execute an operation, such as addition.

 If the operation requires data that isn’t currently available, the GPU can effectively ‘pause’ that thread and work on other threads while waiting for that data. This means that while it can have a significant impact on latency, it allows for very high throughput overall.

### The Synergy Between CPUs and GPUs
The collaborative interplay between CPUs and GPUs brings about a performance enhancement that maximizes the strengths of both processing units. The CPU is efficient at handling a wide variety of tasks, while the GPU excels at executing repetitive calculations. Together, they form a powerful computing duo that can tackle a vast range of applications—from gaming to AI and machine learning.

The synergy between CPUs and GPUs plays a crucial role in the world of computing, allowing for optimized performance and efficiency in data processing tasks. By leveraging the unique strengths of each processor, developers can create applications that maximize their capabilities and achieve significant performance gains.

## GPU Server Systems
Let's take a moment to review GPU server systems. The evolution of GPU computing has brought about significant advancements in server architecture. GPU server systems are designed to harness the power of GPUs to accelerate workloads and improve overall computing performance. 

GPU servers combine the processing capabilities of GPUs with the scalability of server architecture, enabling organizations to deploy AI and machine learning applications at scale. By leveraging the parallel processing capabilities of GPUs, organizations can achieve faster training times and improved performance for complex workloads. 

These systems are built with high-speed interconnects, advanced cooling solutions, and optimized configurations to ensure efficient power consumption and maximum performance. As data demands continue to grow, GPU server systems will play a critical role in enabling organizations to meet the challenges of accelerated computing.

---

# Check Your Knowledge

Here’s the formatted content for your new questions:

---

### 1. Question 1

**What are GPUs optimized for?**

- Controlling the computer system's power supply and cooling.
- Facilitating network communication between computers.
- Storing and managing data.
- Executing highly parallel tasks.

  


---

### 2. Question 2

**What are the key architectural components of a GPU?**  
*(Select Three)*

- GPU cores
- Cooling
- Cache memory
- GPU-specific memory

  


---

### 3. Question 3

**When comparing CPUs and GPUs, what is a key strength of CPUs?**

- High parallel processing capability.
- Specialized graphics rendering.
- General-purpose computing and handling of complex logic.
- Low power consumption.

  

