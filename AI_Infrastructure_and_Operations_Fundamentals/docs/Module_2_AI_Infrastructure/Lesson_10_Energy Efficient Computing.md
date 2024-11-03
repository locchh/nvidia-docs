# Energy Efficient Computing

## Outline
In this unit we will cover:
- Data Center Efficiency Considerations

## Objectives
By the end of this unit, you will be able to:
- Articulate what goes into planning data center deployments including the equipment that will be installed in the data center (Power consumption, Cooling considerations)
- Discuss how NVIDIA optimizes enegy efficency in data centers
- Describe cooling architecure GPUs in data centers
- Understand how to improve through co-location

## Energy-Efficient Computing and Your Data Center

### Learning Objectives

In this unit, we will be focusing on energy-efficient computing and your data center. By the end of this unit, you should be able to thoughtfully articulate the steps in the planning and deployment of a data center, including the equipment that will be installed in the data center.

### Overview

1. **Power Consumption and Cooling Considerations**
2. **Nvidia's Technology Designed for Efficiency**
3. **Mitigation of Negative Impact with Efficient Cooling Systems**
4. **Data Center Colocation and Efficiency**

Nvidia strives for low environmental impact by ensuring GPUs consume fewer resources and run as efficiently as possible. Let's start by covering data center considerations and Nvidia GPU architectures.

### Data Center Deployment Planning

Planning a data center deployment requires a balance between all five of the process domains: 
- Data center operations
- IT operations
- NOC support
- Application owner
- Network operations

These five domains must continuously be coordinated and balanced to ensure a successful deployment. 

At a high level, data center resources can be categorized as power, cooling, and space. Given that data centers have finite resources, a change in one of these resources impacts the other two. This drives the need to optimize resource utilization for efficiency.

### Energy Demand and Resource Utilization

The recent explosion of energy demand in data centers is due to:
- Massive data loads
- Complex data models
- Extreme processing power required to run today's applications and tools

As computing becomes more sophisticated, particularly with AI tools and applications, the demand for data center resources such as power and space has significantly increased. 

Accelerated computing with GPU technology is optimized for efficiency in the data center. Individual GPUs handle large-scale compute-intensive functions with less technology and require less space. 

**Comparison of Workloads:**  
While GPUs require more power consumption, the amount of time the workload runs is significantly reduced. The increase in power consumed at a given time is offset by the fact that the workload runs so quickly, thus using less energy over time.

Another benefit is that multi-instance GPUs allow users to partition the GPU, enabling simultaneous workloads without increasing power consumption. 

Processing capabilities have grown exponentially in the past decade, fueled largely by supercomputers, data centers, and cloud computing. A data center with Nvidia GPUs requires a fraction of the space and energy:
- A hyperscale data center with Nvidia GPUs takes up only 1/47th of the rack space of the CPU-based systems it replaces and runs at 93% lower energy cost for AI models.

### Software and Energy Efficiency

Software can significantly improve the energy efficiency of AI workloads. Nvidia continuously optimizes CUDA-X libraries and GPU-accelerated applications, leading to noticeable performance gains on the same GPU architecture. For example, AI workloads on Nvidia Ampere architecture improved by 2.5x over the past two years. 

Nvidia provides the latest versions of AI and HPC software from the Nvidia GPU Cloud (NGC) portal, helping users run applications with better performance in their supercomputer, data center, or cloud. An estimated energy savings of 20% on NGC workloads is possible through performance suggestions.

### Alleviating CPU Strain

As supercomputers take on more workloads, CPUs are stretched to support the growing number of communication tasks needed to operate large and complex systems. Data Processing Units (DPUs) alleviate over 30% of this stress by offloading processes from the CPU. Some workloads achieve more than 50x performance improvement, allowing fewer servers to be deployed and reducing the power of a modest data center by four megawatts.

The zero-trust protection platform enabled by Nvidia DPUs brings a new level of security to data centers at speeds up to 600 times faster than servers without Nvidia accelerations, further reducing the amount of infrastructure and power required.

### Nvidia Spectrum-4 Ethernet Switch

Built for AI, the Nvidia Spectrum-4 Ethernet switch enables extreme networking performance and robust security with 40% lower power consumption compared to the previous generation.

### Optimizing Cooling for Performance

Adequate cooling is crucial for optimizing supercomputer performance. Nvidia deploys state-of-the-art technology designed for Nvidia server products using computational fluid dynamics models to enhance cooling for data center designs and server rack deployments.

Using physics-informed neural networks (PINNs) available in Nvidia Modulus, Nvidia designs heat sinks for its DGX systems. Cooling solutions are closely coupled with server racks to localize and optimize heat transfer. Nvidia shares its data center best practices with customers and partners to help optimize deployments.

### Reference Architectures

In partnership with leading storage and networking technology providers, Nvidia offers a portfolio of reference architectures for optimal and efficient deployment of DGX server products, available publicly on its corporate website.

### Energy Efficiency Analysis

One of the superpowers of accelerated computing is energy efficiency in terms of application throughput per kilowatt hour. A simple study of several common HPC applications shows that the HGX H100 4x GPU system has a geo mean performance advantage of 22.9X compared to a dual-socket Sapphire Rapids system. 

Estimating annual energy use:
- **HGX supercomputer (50 nodes):** 2.6 gigawatt hours 
- **CPU system (1,150 servers):** 12.1 gigawatt hours 

This indicates a significant energy efficiency advantage for the accelerated platform.

### Comparing A100 and H100 for AI Workloads

When comparing data requirements and compute capabilities of the A100 versus the H100 for deploying AI workloads:
- The H100 requires fewer servers while managing the same workload as significantly more A100s.
- For example, 64 H100s achieve a third of the total cost of ownership (TCO) using a fifth of the server nodes and is 3.5 times more energy efficient.

The DGX H100 system is the compute building block of the DGX SuperPOD, offering extreme performance benefits for AI workloads. It has specific power, environmental, and cooling requirements for optimal operation, including maintaining air temperature between 5-30°C (41-86°F).

### Data Center Cooling Optimization

Now that we've discussed Nvidia's approaches to reduce rack space and power consumption, let’s talk about data center cooling and how Nvidia optimizes cooling to improve efficiency.

#### Cooling Options:

1. **Cold Air Cooling:** 
   - Inexpensive but limited to cooling 30 kilowatts per rack.

2. **Water-Cooled Heat Exchangers:** 
   - More efficient but more expensive; can serve between 20-60 kilowatts per rack, with some manufacturers claiming over 100 kilowatts.

### Cooling Process Steps

**Direct Air-Cooled Systems:**  
- CRAHs (Computer Room Air Handling units) circulate chilled water through coils and use large fans to blow hot air over these coils to absorb heat.
- Cold air is pressurized under the server room floor and distributed to all systems and racks.
- Hot air from the systems is drawn back to the CRAH units, where heat is transferred to the chilled water inside the coils.

The hot aisle/cold aisle layout optimizes airflow and cooling efficiency in a data center. Installing blanking panels wherever possible is crucial to ensure proper airflow throughout the data center rack.

### Alternative Cooling Option

**Heat Rejection to Air or Water:**  
- Characteristics include rear doors with chilled water coils positioned six inches from servers, capturing heat from the servers and transferring it externally for dissipation. 
- Rear door heat exchangers are often used in solid or slab floor facilities, while cold aisle containment systems are typically deployed in raised floor facilities.

### Power Provisioning

Data center power provisioning must be completed prior to connecting power to the in-rack power distribution units (PDUs) and system deployment. Nvidia recommends each component be supplied with redundant power sources to increase system reliability. 

AC power redundancy should be validated at each rack. An electrician or facility representative must verify that the AC voltage and total kilowatts supplied meet specifications at each floor-mounted PDU and individual circuits (power drops feeding the racks). The equipment served by each circuit breaker within the PDU should be clearly labeled.

### DGX Data Center Colocation Program

Let’s discuss the benefits of Nvidia's DGX data center colocation program in saving resources and improving overall efficiency. 

Businesses are increasingly aware of the advantages of accelerated computing with GPUs. Nvidia and its partners lead the adoption of GPU computing in data centers. DGX-based systems offer unprecedented compute density to tackle the world's most complex AI challenges and have been rapidly adopted by various organizations across multiple sectors (e.g., internet service companies, healthcare facilities, government labs, financial institutions, oil and gas businesses).

However, some businesses lack modern data center facilities to support accelerated computing operations. A single DGX H100 system draws a maximum of 10.2 kilowatts. Nvidia's current DGX SuperPOD reference architecture exceeds 40 kilowatts per rack, while many enterprises can only support 8-15 kilowatts per rack in their existing data centers.

The Nvidia DGX-ready data center program pairs businesses with the best partners for their needs, available in Asia, Australia, Europe, North America, and South America. Select partners provide a broader range of services, including test drive and GPU-as-a-service offerings.

Through colocation, customers can avoid facilities planning challenges or high costs and latency of the public cloud, allowing them to focus on gaining insights from data while innovating. The program facilitates the deployment of Nvidia DGX systems and recently announced DGX reference architecture solutions from various partners, offering speed and simplicity at an affordable OpEx model.

### Commitment to Net Zero

Nvidia continues to strive for a net-zero data center with improvements across GPU hardware and networking equipment from generation to generation. Significant advancements from Ampere to Hopper, combined with the ability to run AI workloads faster and more efficiently, reduce GPU usage time.

For example, the Nvidia Ampere GPU architecture introduced TF32 math mode for accelerating single-precision deep learning

 training, achieving the same accuracy as FP32 training while providing 10x faster tensor math than single-precision math on Volta GPUs.

### Conclusion

Now that you've completed this unit, you should be able to:
- Articulate the design and planning of a data center.
- Understand how space, power, and cooling considerations affect plans.
- Discuss how Nvidia's methods and servers optimize energy efficiency in data centers.
- Describe the cooling architecture of GPUs to improve efficiency.
- Understand how colocation improves efficiency.

Don’t stop here! Continue your learning journey with Unit 11, **AI Reference Architectures**. See you there!

## Keywords
Here are the keywords extracted from the provided text:

- Energy-efficient computing
- Data center
- Learning objectives
- Planning and deployment
- Power consumption
- Cooling considerations
- Nvidia technology
- Efficiency
- Data center colocation
- Environmental impact
- GPUs (Graphics Processing Units)
- Resource utilization
- Energy demand
- Accelerated computing
- CPU vs. GPU
- Performance improvement
- Data processing units (DPUs)
- Zero-trust protection platform
- Security
- Cooling technology
- Computational fluid dynamics
- Physics-informed neural networks (PINNs)
- Power and cooling requirements
- Rack space
- Thermal design power (TDP)
- Performance gain
- DGX systems
- HPC (High Performance Computing)
- AI workloads
- GPU architectures
- Cooling options
- Cold air cooling
- Water-cooled heat exchangers
- CRAH (Computer Room Air Handling units)
- Power provisioning
- Redundant power sources
- DGX data center colocation program
- GPU computing
- Net zero data center
- Ampere architecture
- TF32 math mode
- Summary of learning

These keywords capture the key concepts and topics discussed in the unit.