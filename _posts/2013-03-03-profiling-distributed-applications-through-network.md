---
layout: post
title: "Profiling Distributed Applications Through Network Traffic Analysis"
categories: Pesquisa
tag: mestrado
---

This is the research conducted by Thiago Vieira, which studies techniques for profiling distributed applications at runtime, with low intrusion, high accuracy and fast results.

Distributed systems has been adopted for building modern Internet services and cloud computing infrastructure, in order to obtain services with high performance, scalability and reliability. Cloud computing SLAs require low time to identify, diagnose and solve problems in a cloud computing production infrastructure, in order to avoid problem impacts into the quality of service provided for its clients.

![image](https://github.com/assertlab/assertlab.github.io/_posts/2013-03-03-profiling-distributed-applications-through-network/figura1.png)&nbsp;

The detection of error causes, diagnose and reproduction of errors are challenges that motivate efforts to the development of less intrusive mechanisms for monitoring and debugging distributed applications at runtime.

![image](https://github.com/assertlab/assertlab.github.io/_posts/2013-03-03-profiling-distributed-applications-through-network/figura2.png)

Network traffic analysis is one option to the distributed systems measurement, although there are limitations on capacity to process large amounts of network traffic in short time, and on scalability to process network traffic where there is variation of resource demand.&nbsp;

The goal of this research is to evaluate the processing capacity problem for profiling distributed systems through network traffic analysis, in order to evaluate distributed applications at a data center, using commodity hardware and cloud computing services, in a minimally intrusive way.

We proposed a new approach based on MapReduce, for deep inspection of distributed application traffic, in order to evaluate the behavior of distributed systems at runtime, using commodity hardware. In this research we evaluated the effectiveness of MapReduce for a deep packet inspection algorithm, its processing capacity, completion time speedup, processing capacity scalability, and the behavior followed by MapReduce phases, when applied to deep packet inspection for extracting indicators of distributed applications.

![image](https://github.com/assertlab/assertlab.github.io/_posts/2013-03-03-profiling-distributed-applications-through-network/figura3.png)

With our proposed approach, it is possible to measure the network traffic behavior of distributed applications with intensive network traffic generation, through the offline evaluation of information from the production environment of a distributed system, making it possible to use the information from the evaluated indicators, to diagnose problems and analyse performance of distributed systems.

We showed that MapReduce programming model can express algorithms for DPI, as the algorithm implemented to extract application indicators from the network traffic of a JXTA-based distributed application. We analysed the completion time scalability achieved for different number of nodes in a Hadoop cluster composed of virtual machines, with different size of network traffic used as input. We showed the processing capacity and the completion time scalability achieved, and also was showed the influence of the number of nodes and the data input size in the processing capacity for DPI using virtual machines of Amazon EC2.

We evaluated the performance of MapReduce for packet level analysis and DPI of applications traffic, using commodity hardware, and showed how data input size, block size and cluster size cause relevant impacts into MapReduce phases, job completion time, processing capacity scalability and in the speedup achieved in comparison against the same execution by a non distributed implementation.

The results showed that although MapReduce presents a good processing capacity using cloud services or commodity computers for dealing with massive application traffic analysis, but it is necessary to evaluate the behaviour of MapReduce to process specifics data type, to understand its relation with the available resources and the configuration of MapReduce parameters, and to obtain an optimal performance for specific environments.

We showed that MapReduce processing capacity scalability is not proportional to number of allocated nodes, and the relative processing capacity decreases with node addition. We showed that input size, block size and cluster size are important factors to be considered to achieve better job completion time and to explore MapReduce scalability, due to the observed variation in completion time provided by different block size adopted. Also, in some cases, the processing capacity does not scale with node addition into the cluster, what highlights the importance of allocating resources according with the workload and input data, in order to avoid wasting resources.

We verified that packet level analysis and DPI are Map-intensive jobs, due to Map phase consumes more than 70\% of the total job completion time, and shuffle phase is the second predominant phase. We also showed that using whole block as input for Map functions, was achieved a poor completion time than the approach which splits the block into records.

We published the papers below about this research:

<http://bit.ly/WDryaG>

<http://bit.ly/WDrGXr>

If you want to know more about our research, contact me at **tpbv at cin dot ufpe dot br**.