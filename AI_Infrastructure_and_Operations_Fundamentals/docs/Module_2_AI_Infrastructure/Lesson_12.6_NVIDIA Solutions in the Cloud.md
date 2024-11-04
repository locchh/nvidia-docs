# NVIDIA Solutions in the Cloud

In this final subunit, we'll explore NVIDIA's AI cloud-based solutions and how they can help you harness the power of AI in the cloud.

### Overview of the NVIDIA AI Platform
The NVIDIA AI platform is designed to address the challenges of enterprise AI and meet customers where they are. With this full-stack platform, enterprises can use the power of AI to deliver business results, irrespective of where they are in their AI adoption journey. 

The NVIDIA AI platform is cloud-native, allowing customers to develop and deploy AI-enabled applications anywhere—from any public cloud to enterprise data centers to edge locations—without being locked into any one cloud or deployment option.

Using this stack as a reference, we'll look at what each layer of the NVIDIA AI platform looks like in the public cloud and the different ways to drive the consumption of NVIDIA technology for cloud customers.

### Accelerated Infrastructure
Let's start at the bottom of the stack and work our way up. The foundation of the NVIDIA AI platform is accelerated infrastructure, which in the context of cloud computing refers to virtual machine instances equipped with NVIDIA GPUs. 

Additionally, some cloud service providers (CSPs) incorporate NVIDIA networking technologies to achieve at-scale performance. The NVIDIA virtual machine images (VMIs) available through CSP marketplaces underlie application software, whether sourced from the NGC catalog or generic AI software. 

NVIDIA VMIs provide an operating system environment for running NVIDIA GPU-accelerated software in the cloud. These VM images are built on top of Ubuntu OS and are packaged with core dependencies. VMIs provide a GPU-optimized development environment for your GPU-accelerated application on a cloud service provider's infrastructure. 

VMIs are essentially the operating system for cloud VMs, sitting on top of cloud instance types. A cloud instance type is a predefined virtual server configuration provided by a cloud service provider, specifying computing resources like CPU, memory, storage, and networking for virtual machines. 

Users choose instance types based on workload, scalability, and budget, with options like general-purpose, compute-optimized, memory-optimized, and GPU instances. 

### NVIDIA AI Enterprise
Now that you've grasped the cloud-accelerated infrastructure layer, let's ascend the NVIDIA AI stack to touch briefly on NVIDIA AI Enterprise. 

The next layer is the API platform software layer. NVIDIA AI Enterprise is the AI platform software layer. Software enables enterprise AI applications to leverage the power of the underlying accelerated infrastructure. 

Application performance has a direct tie-in to operational costs in the cloud, which is why you want to ensure you're always getting the most of your compute resources. With NVIDIA optimized and enterprise-supported software, customers can achieve both the best performance from the accelerated infrastructure and accelerate time to solution.

While we covered NVIDIA AI Enterprise in unit five, it's essential to emphasize its deployability in the cloud. In fact, NVIDIA AI Enterprise represents a secure, end-to-end, and cloud-native AI software platform specifically designed for production AI workloads. The solution is available across multiple deployment environments, including public, hybrid, and multi-clouds.

### NVIDIA NGC Catalog
Another key component of the AI platform in the cloud is NGC. Let's explore that next. 

NVIDIA NGC serves as a central hub for all NVIDIA services, software, and support, providing customers with a one-stop shop for our AI offerings. With a subscription or license to NVIDIA AI Enterprise, customers gain access to the enterprise catalog hosted on NGC, which includes AI workflows and new AI services.

However, free software access through NGC does not provide the same level of benefits as NVIDIA AI Enterprise, such as enterprise support, SLAs, access to NVIDIA AI experts, and exclusive enterprise product differentiators.

### AI Services Layer
Let's continue up the NVIDIA AI platform stack to AI services. The topmost layer of the NVIDIA AI platform is the AI services layer; this is the newest addition to the NVIDIA cloud portfolio. It is the highest level of abstraction at which customers can engage with our platform. It brings to bear the value of the entire NVIDIA AI platform to the end customer as an NVIDIA managed service.

#### NVIDIA DGX Cloud
Let's start with NVIDIA DGX Cloud and work our way up the AI services. Consider the following: with traditional AI development on traditional clouds, DIY tools and open-source software are used to patch together a solution. 

This results in inconsistent access to multinode scaling across regions, searching through community forums, and voluntary contributions to find answers to your questions, if you're lucky. Escalating costs, add-on fees for reserved instances, storage, and data egress complicate the process.

NVIDIA DGX Cloud is a multinode AI training-as-a-service solution for enterprise AI. When a model is too large to fit into a GPU's memory, multinode training is advantageous, all within a single service offered at an all-in-one monthly price. It brings together the NVIDIA Base Command platform, NVIDIA AI Enterprise software, and NVIDIA DGX infrastructure combined with access to NVIDIA AI expertise and support. 

Customers can just open a browser to get started without having to procure, set up, and manage an AI supercomputer on their own. As a service, DGX Cloud is hosted across multiple public clouds like Oracle Cloud Infrastructure, Microsoft Azure, and Google Cloud.

### NVIDIA AI Foundations
Having gained a fundamental comprehension of the DGX Cloud solution, let us delve into the realm of NVIDIA AI Foundations. NVIDIA AI Foundations is another suite of NVIDIA-managed cloud services powered by the NVIDIA DGX Cloud.

NVIDIA AI Foundations is a set of cloud services for enterprises to build and run custom generative AI by leveraging state-of-the-art foundation models for text, language, visual media, and biology. There are currently two collections that are part of the NVIDIA AI Foundations.

NVIDIA introduced the NeMo-3-8B enterprise-ready family of models, which have been trained using responsibly sourced data. These models deliver results comparable to larger models but with a reduced inference cost. Ideal for global enterprises, these models support over 50 spoken and 35 coding languages. They find applications in various scenarios such as chat and Q&A applications across diverse industries, including healthcare, telecommunications, and financial services.

Community models optimized by NVIDIA for both throughput and latency using TensorRT LLM ensure the utmost performance efficiency. Achieving a 2x higher inference on LLAMA 2 with TRT LLM, these models include LLAMA 2, Mistral, Stable Diffusion, and Code Llama. 

Streamlined for customization, all models are converted to the NeMo format. This allows developers to make the most of NeMo's data preparation guardrails and advanced customization techniques, facilitating the fine-tuning of these foundational models with proprietary data on DGX Cloud.

Explore the models using the fully accelerated NVIDIA AI stack. Test the models directly from your browser through a GUI or app without the need for additional setup. Seamlessly connect enterprise applications to NVIDIA-hosted API endpoints to assess the full potential of the models in real-world applications. These models can be found in the NVIDIA NGC catalog, are accessible on several CSPs, and are also featured on the Hugging Face website.

### NVIDIA AI Foundry
Let's delve into the uppermost tier of the NVIDIA AI services stack known as NVIDIA AI Foundry. An AI Foundry is a new kind of service for creating custom generative AI models. The service should provide pioneering state-of-the-art pre-trained models, utilities for effortless customization of models with proprietary data, and cloud-native infrastructure with accelerated capabilities. 

These elements come together to enable the creation of customized enterprise-grade models at scale. The NVIDIA AI Foundry service gives enterprises an end-to-end solution for creating custom generative AI models. It encapsulates three elements:

1. **NVIDIA AI Foundation Models**: This encompasses state-of-the-art, pre-trained models from NVIDIA, along with NVIDIA optimized community foundation models, which are hosted in CSPs' model catalogs.

2. **NVIDIA NeMo Framework**: Provides tools for fine-tuning models with enterprise-grade runtime, incorporating guardrails, optimizations, and advanced customization techniques.

3. **NVIDIA DGX Cloud**: This is a serverless AI training-as-a-service platform for enterprise developers that runs on various hyperscalers and is first being introduced with Microsoft Azure.

Users can rent NVIDIA DGX Cloud, now available on Azure, which comes with NVIDIA AI Enterprise, including NeMo to speed LLM customization. The output is a custom model container tuned with proprietary data, guardrails, and inference runtime. Once customized, these enterprise proprietary models can be deployed virtually anywhere on accelerated computing with enterprise-grade security, stability, and support using NVIDIA AI Enterprise.

### Conclusion
Let's end the unit with a review of the ways in which you can consume NVIDIA solutions on the cloud. 

In summary, the effective deployment and utilization of AI capabilities in the cloud require a keen focus on consumption, encompassing both the allocation of cloud resources and the optimization of associated costs, in order to unlock the full potential of AI in driving business success.

NVIDIA accelerated infrastructure in the cloud is the foundational piece of making our technology available broadly to cloud customers. However, NVIDIA has come a long way from doing just that and has built an entire full-stack platform that can now be consumed in the cloud. 

Be it full-stack consumption with the AI services provided with DGX Cloud, AI Foundations, or AI Foundry AI services; software and infrastructure consumption with NVIDIA AI Enterprise software; or infrastructure consumption with different layers of the NVIDIA AI platform combined with our integrations on CSPs, customers have a path to use and derive value from NVIDIA, even within cloud services that they may already use today.

### Learning Outcomes
Now that you've completed this unit, you should be able to:
- Explain the various ways cloud computing enhances AI deployments.
- Describe the wide variety of AI use cases in cloud computing environments.
- Outline the key considerations and strategies when deploying AI in the cloud.
- Summarize the wide variety of cloud service providers that support NVIDIA technologies and solutions.


- Categorize the various cloud consumption models when deciding how to consume cloud services.
- Evaluate NVIDIA's cloud solutions and how they can benefit your workloads.

Concluding this unit marks a significant milestone in our journey through the introduction to AI in the data center course. Fantastic progress so far! As we look forward, we're set to explore Unit 13: AI Data Center Management and Monitoring. See you in the next unit!

# Check Your Knowledge

**Question 1**  
Your manager has asked you to evaluate moving AI workloads to the cloud.  

What key considerations should be evaluated when assessing the move of AI workloads to the cloud?  
*(Choose four)*  

- Compatibility with Kubernetes  
- Data locality  
- Hybrid IT strategies  
- Real-time performance  
- Data sovereignty  

**Answers:**  
- Data locality  
- Hybrid IT strategies  
- Real-time performance  
- Data sovereignty  