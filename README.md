# Awesome Bigdata papers
A curated list of  Big data papers reading for anyone who are eager to learn!


1. [The Hadoop Distributed File System](http://storageconference.us/2010/Papers/MSST/Shvachko.pdf) 
> Abstract - The Hadoop Distributed File System (HDFS) is designed to store very large data sets reliably, and to stream those data sets at high bandwidth to user applications. In a large cluster, thousands of servers both host directly attached storage and execute user application tasks. By distributing storage and computation across many servers, the resource can grow with demand while remaining economical at every size. We describe the architecture of HDFS and report on experience using HDFS
to manage 25 petabytes of enterprise data at Yahoo!.

2. [Resilient Distributed Datasets: A Fault-Tolerant Abstraction for In-Memory Cluster Computing](https://www.usenix.org/system/files/conference/nsdi12/nsdi12-final138.pdf)
>Abstract - We present Resilient Distributed Datasets (RDDs), a distributed memory abstraction that lets programmers perform in-memory computations on large clusters in a fault-tolerant manner. RDDs are motivated by two types of applications that current computing frameworks handle inefficiently: iterative algorithms and interactive data mining tools. In both cases, keeping data in memory can improve performance by an order of magnitude. To achieve fault tolerance efficiently, RDDs provide a restricted form of shared memory, based on coarsegrained transformations rather than fine-grained updates to shared state. However, we show that RDDs are expressive enough to capture a wide class of computations, including recent specialized programming models for iterative jobs, such as Pregel, and new applications that these models do not capture. We have implemented RDDs in a system called Spark, which we evaluate through a variety of user applications and benchmarks.

3. [Spark SQL: Relational Data Processing in Spark](https://pages.databricks.com/rs/094-YMS-629/images/SparkSQLSigmod2015.pdf)
> Abstract- Spark SQL is a new module in Apache Spark that integrates relational processing with Spark’s functional programming API. Built on our experience with Shark, Spark SQL lets Spark programmers leverage the benefits of relational processing (e.g., declarative queries and optimized storage), and lets SQL users call complex analytics libraries in Spark (e.g., machine learning). Compared to previous systems, Spark SQL makes two main additions. First, it offers much tighter integration between relational and procedural processing, through a declarative DataFrame API that integrates with procedural Spark code. Second, it includes a highly extensible optimizer, Catalyst, built using features of the Scala programming language, that makes it easy to add composable rules, control code generation, and define extension points. Using Catalyst, we have built a variety of features (e.g., schema inference for JSON, machine learning types, and query federation to external databases) tailored for the complex needs of modern data analysis. We see Spark SQL as an evolution of both SQL-on-Spark and of Spark itself, offering richer APIs and optimizations while keeping the benefits of the Spark programming model.

4. [Storm @Twitter](https://cs.brown.edu/courses/cs227/archives/2015/papers/ss-storm.pdf)
> Abstract - This paper describes the use of Storm at Twitter. Storm is a realtime fault-tolerant and distributed stream data processing system. Storm is currently being used to run various critical computations in Twitter at scale, and in real-time. This paper describes the architecture of Storm and its methods for distributed scale-out and fault-tolerance. This paper also describes how queries (aka. topologies) are executed in Storm, and presents some operational stories based on running Storm at Twitter. We also present results from an empirical evaluation demonstrating the resilience of Storm in dealing with machine failures. Storm is under active development at Twitter and we also present some potential directions for future work. 

5. [Apache Flink: Stream Analytics at Scale](https://www.researchgate.net/publication/305869785_Apache_Flink_Stream_Analytics_at_Scale)
> Abstract - Apache Flink is an open-source system for processing streaming and batch data. Flink is built on the philosophy that many classes of data processing applications, including real-time analytics, continuous data pipelines, historic data processing (batch), and iterative algorithms (machine learning, graph analysis) can be expressed and executed as pipelined fault-tolerant dataflows. In this paper, we present Flink’s architecture and expand on how a (seemingly diverse) set of use cases can be unified under a single execution model.

6. [Twitter Heron: Stream Processing at Scale](https://dl.acm.org/citation.cfm?id=2742788)
> Abstract - Storm has long served as the main platform for real-time analytics at Twitter. However, as the scale of data being processed in realtime at Twitter has increased, along with an increase in the diversity and the number of use cases, many limitations of Storm have become apparent. We need a system that scales better, has better debug-ability, has better performance, and is easier to manage – all while working in a shared cluster infrastructure. We considered various alternatives to meet these needs, and in the end concluded that we needed to build a new real-time stream data processing system. This paper presents the design and implementation of this new system, called Heron. Heron is now the de facto stream data processing engine inside Twitter, and in this paper we also share our experiences from running Heron in production. In this paper, we also provide empirical evidence demonstrating the efficiency and scalability of Heron.

7. [Lightweight Asynchronous Snapshots for Distributed Dataflows](https://arxiv.org/pdf/1506.08603.pdf)
> Abstarct - Distributed stateful stream processing enables the deployment and execution of large scale continuous computations in the cloud, targeting both low latency and high throughput. One of the most fundamental challenges of this paradigm is providing processing guarantees under potential failures. Existing approaches rely on periodic global state snapshots that can be used for failure recovery. Those approaches suffer from two main drawbacks. First, they often stall the overall computation which impacts ingestion. Second, they eagerly persist all records in transit along with the operation states which results in larger snapshots than required. In this work we propose Asynchronous Barrier Snapshotting (ABS), a lightweight algorithm suited for modern dataflow execution engines that minimises space requirements. ABS persists only operator states on acyclic execution topologies while keeping a minimal record log on cyclic dataflows. We implemented ABS on Apache Flink, a distributed analytics engine that supports stateful stream processing. Our evaluation shows that our algorithm does not have a heavy impact on the execution, maintaining linear scalability and performing well with frequent snapshots.

8. [Naiad: A Timely Dataflow System](https://pdos.csail.mit.edu/6.824/papers/naiad.pdf)
> Abstarct - Naiad is a distributed system for executing data parallel, cyclic dataflow programs. It offers the high throughput of batch processors, the low latency of stream processors, and the ability to perform iterative and incremental computations. Although existing systems offer some of these features, applications that require all three have relied on multiple platforms, at the expense of efficiency, maintainability, and simplicity. Naiad resolves the complexities of combining these features in one framework. A new computational model, timely dataflow, underlies Naiad and captures opportunities for parallelism across a wide class of algorithms. This model enriches dataflow computation with timestamps that represent logical points in the computation and provide the basis for an efficient, lightweight coordination mechanism. We show that many powerful high-level programming models can be built on Naiad’s low-level primitives, enabling such diverse tasks as streaming data analysis, iterative machine learning, and interactive graph mining. Naiad outperforms specialized systems in their target application domains, and its unique features enable the development of new high-performance applications.

9. [The Dataflow Model: A Practical Approach to Balancing Correctness, Latency, and Cost in Massive-Scale, Unbounded, Out-of-Order Data Processing](http://people.csail.mit.edu/matei/courses/2015/6.S897/readings/google-dataflow.pdf)
> Abstarct - Unbounded, unordered, global-scale datasets are increasingly common in day-to-day business (e.g. Web logs, mobile usage statistics, and sensor networks). At the same time, consumers of these datasets have evolved sophisticated requirements, such as event-time ordering and windowing by features of the data themselves, in addition to an insatiable hunger for faster answers. Meanwhile, practicality dictates that one can never fully optimize along all dimensions of correctness, latency, and cost for these types of input. As a result, data processing practitioners are left with the quandary of how to reconcile the tensions between these seemingly competing propositions, often resulting in disparate implementations and systems. We propose that a fundamental shift of approach is necessary to deal with these evolved requirements in modern data processing. We as a field must stop trying to groom unbounded datasets into finite pools of information that eventually become complete, and instead live and breathe under the assumption that we will never know if or when we have seen all of our data, only that new data will arrive, old data may be retracted, and the only way to make this problem tractable is via principled abstractions that allow the practitioner the choice of appropriate tradeoffs along the axes of interest: correctness, latency, and cost. In this paper, we present one such approach, the Dataflow Model , along with a detailed examination of the semantics it enables, an overview of the core principles that guided its design, and a validation of the model itself via the real-world experiences that led to its development.

10. [MillWheel: Fault-Tolerant Stream Processing at Internet Scale](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/41378.pdf)
> Abstarct - MillWheel is a framework for building low-latency data-processing applications that is widely used at Google. Users specify a directed computation graph and application code for individual nodes, and the system manages persistent state and the continuous flow of records, all within the envelope of the framework's fault-tolerance guarantees. This paper describes MillWheel's programming model as well as its implementation. The case study of a continuous anomaly detector in use at Google serves to motivate how many of MillWheel's features are used. MillWheel's programming model provides a notion of logical time, making it simple to write time-based aggregations. MillWheel was designed from the outset with fault tolerance and scalability in mind. In practice, we find that MillWheel's unique combination of scalability, fault tolerance, and a versatile programming model lends itself to a wide variety of problems at Google.

11. [MapReduce: Simplified Data Processing on Large Clusters](https://static.googleusercontent.com/media/research.google.com/en//archive/mapreduce-osdi04.pdf)
> Abstarct - MapReduce is a programming model and an associated implementation for processing and generating large data sets. Users specify a map function that processes a key/value pair to generate a set of intermediate key/value pairs, and a reduce function that merges all intermediate values associated with the same intermediate key. Many real world tasks are expressible in this model, as shown in the paper. Programs written in this functional style are automatically parallelized and executed on a large cluster of commodity machines. The run-time system takes care of the details of partitioning the input data, scheduling the program's execution across a set of machines, handling machine failures, and managing the required inter-machine communication. This allows programmers without any experience with parallel and distributed systems to easily utilize the resources of a large distributed system. Our implementation of MapReduce runs on a large cluster of commodity machines and is highly scalable: a typical MapReduce computation processes many terabytes of data on thousands of machines. Programmers find the system easy to use: hundreds of MapReduce programs have been implemented and upwards of one thousand MapReduce jobs are executed on Google's clusters every day.

12. [Bigtable: A Distributed Storage System for Structured Data](https://static.googleusercontent.com/media/research.google.com/en//archive/bigtable-osdi06.pdf)
> Abstarct - Bigtable is a distributed storage system for managing structured data that is designed to scale to a very large size: petabytes of data across thousands of commodity servers. Many projects at Google store data in Bigtable, including web indexing, Google Earth, and Google Finance. These applications place very different demands on Bigtable, both in terms of data size (from URLs to web pages to satellite imagery) and latency requirements (from backend bulk processing to real-time data serving). Despite these varied demands, Bigtable has successfully provided a flexible, high-performance solution for all of these Google products. In this paper we describe the simple data model provided by Bigtable, which gives clients dynamic control over data layout and format, and we describe the design and implementation of Bigtable.

13. [The Google File System](https://static.googleusercontent.com/media/research.google.com/en//archive/gfs-sosp2003.pdf)
> Abstarct - We have designed and implemented the Google File System, a scalable distributed file system for large distributed data-intensive applications. It provides fault tolerance while running on inexpensive commodity hardware, and it delivers high aggregate performance to a large number of clients. While sharing many of the same goals as previous distributed file systems, our design has been driven by observations of our application workloads and technological environment, both current and anticipated, that reflect a marked departure from some earlier file system assumptions. This has led us to reexamine traditional choices and explore radically different design points. The file system has successfully met our storage needs. It is widely deployed within Google as the storage platform for the generation and processing of data used by our service as well as research and development efforts that require large data sets. The largest cluster to date provides hundreds of terabytes of storage across thousands of disks on over a thousand machines, and it is concurrently accessed by hundreds of clients. In this paper, we present file system interface extensions designed to support distributed applications, discuss many aspects of our design, and report measurements from both micro-benchmarks and real world use.

14. [Pilot-Streaming: A Stream Processing Framework for High-Performance Computing](https://arxiv.org/pdf/1801.08648.pdf)
> Abstarct - An increasing number of scientific applications rely on stream processing for generating timely insights from data feeds of scientific instruments, simulations, and Internet-of-Thing (IoT) sensors. The development of streaming applications is a complex task and requires the integration of heterogeneous, distributed infrastructure, frameworks, middleware and application components. Different application components are often written in different languages using different abstractions and frameworks. Often, additional components, such as a message broker (e. g. Kafka), are required to decouple data production and consumptions and avoiding issues, such as back-pressure. Streaming applications may be extremely dynamic due to factors, such as variable data rates caused by the data source, adaptive sampling techniques or network congestions, variable processing loads caused by usage of different machine learning algorithms. As a result application-level resource management that can respond to changes in one of these factors is critical. We propose Pilot- Streaming, a framework for supporting streaming frameworks, applications and their resource management needs on HPC infrastructure. Pilot-Streaming is based on the Pilot-Job concept and enables developers to manage distributed computing and data resources for complex streaming applications. It enables applications to dynamically respond to resource requirements by adding/removing resources at runtime. This capability is critical for balancing complex streaming pipelines. To address the complexity in developing and characterization of streaming applications, we present the Streaming Mini- App framework, which supports different plug-able algorithms for data generation and processing, e. g., for reconstructing light source images using different techniques. We utilize the Mini-App framework to conduct an evaluation of the Pilot-Streaming capabilities.

15. [Apache Tez: A Unifying Framework for Modeling and Building Data Processing Applications](http://web.eecs.umich.edu/~mosharaf/Readings/Tez.pdf)
> Abstarct - The broad success of Hadoop has led to a fast-evolving and diverse ecosystem of application engines that are building upon the YARN resource management layer. The open-source implementation of MapReduce is being slowly replaced by a collection of engines dedicated to specific verticals. This has led to growing fragmentation and repeated efforts—with each new vertical engine re-implementing fundamental features (e.g. fault-tolerance, security, stragglers mitigation, etc.) from scratch. In this paper, we introduce Apache Tez, an open-source framework designed to build data-flow driven processing runtimes. Tez provides a scaffolding and library components that can be used to quickly build scalable and efficient data-flow centric engines. Central to our design is fostering component re-use, without hindering customizability of the performance-critical data plane. This is in fact the key differentiator with respect to the previous generation of systems (e.g. Dryad, MapReduce) and even emerging ones (e.g. Spark), that provided an d mandated a fixed data plane implementation. Furthermore, Tez provides native support to build runtime optimizations, such as dynamic partition pruning for Hive. Tez is deployed at Yahoo!, Microsoft Azure, LinkedIn and numerous Hortonworks customer sites, and a growing number of engines are being integrated with it. This confirms our intuition that most of the popular vertical engines can leverage a core set of building blocks. We complement qualitative accounts of real-world adoption with quantitative experimental evidence that Tez-based implementations of Hive, Pig, Spark, and Cascading on YARN outperform their original YARN implementation on popular benchmarks (TPC-DS, TPC-H) and production workloads.

16. [Realtime Data Processing at Facebook](https://research.fb.com/wp-content/uploads/2016/11/realtime_data_processing_at_facebook.pdf)
> Abstarct - Realtime data processing powers many use cases at Facebook, including realtime reporting of the aggregated, anonymized voice of Facebook users, analytics for mobile applications, and insights for Facebook page administrators. Many companies have developed their own systems; we have a realtime data processing ecosystem at Facebook that handles hundreds of Gigabytes per second across hundreds of data pipelines. Many decisions must be made while designing a realtime stream processing system. In this paper, we identify five important design decisions that affect their ease of use, performance, fault tolerance, scalability, and correctness. We compare the alternative choices for each decision and contrast what we built at Facebook to other published systems. Our main decision was targeting seconds of latency, not milliseconds. Seconds is fast enough for all of the use cases we support and it allows us to use a persistent message bus for data transport. This data transport mechanism then paved the way for fault tolerance, scalability, and multiple options for correctness in our stream processing systems Puma, Swift, and Stylus. We then illustrate how our decisions and systems satisfy our requirements for multiple use cases at Facebook. Finally, we reflect on the lessons we learned as we built and operated these systems.

17. [Fuxi: a Fault-Tolerant Resource Management and Job Scheduling System at Internet Scale](http://www.vldb.org/pvldb/vol7/p1393-zhang.pdf)
> Abstarct - Scalability and fault-tolerance are two fundamental challenges for all distributed computing at Internet scale. Despite many recent advances from both academia and industry, these two problems are still far from settled. In this paper, we present Fuxi, a resource management and job scheduling system that is capable of handling the kind of workload at Alibaba where hundreds of terabytes of data are generated and analyzed everyday to help optimize the company’s business operations and user experiences. We employ several novel techniques to enable Fuxi to perform efficient scheduling of hundreds of thousands of concurrent tasks over large clusters with thousands of nodes: 1) an incremental resource management protocol that supports multi-dimensional resource allocation and data locality; 2) user-transparent failure recovery where failures of any Fuxi components will not impact the execution of user jobs; and 3) an effective detection mechanism and a multi-level blacklisting scheme that prevents them from affecting job execution. Our evaluation results demonstrate that 95% and 91% scheduled CPU/memory utilization can be fulfilled under synthetic workloads, and Fuxi is capable of achieving 2.36TB/minute throughput in GraySort. Additionally, the same Fuxi job only experiences approximately 16% slowdown under a 5% fault-injection rate. The slowdown only grows to 20% when we double the fault-injection rate to 10%. Fuxi has been deployed in our production environment since 2009, and it now manages hundreds of thousands of server nodes.

18. [Dryad: Distributed Data-parallel Programs from Sequential Building Blocks](https://www.microsoft.com/en-us/research/wp-content/uploads/2007/03/eurosys07.pdf)
> Abstarct - Dryad is a general-purpose distributed execution engine for coarse-grain data-parallel applications. A Dryad application combines computational “vertices” with communication “channels” to form a dataflow graph. Dryad runs the application by executing the vertices of this graph on a set of available computers, communicating as appropriate through files, TCP pipes, and shared-memory FIFOs. The vertices provided by the application developer are quite simple and are usually written as sequential programs with no thread creation or locking. Concurrency arises from Dryad scheduling vertices to run simultaneously on multiple computers, or on multiple CPU cores within a computer. The application can discover the size and placement of data at run time, and modify the graph as the computation progresses to make efficient use of the available resources. Dryad is designed to scale from powerful multi-core single computers, through small clusters of computers, to data centers with thousands of computers.

19. [Spark: Cluster Computing with Working Sets](http://static.usenix.org/legacy/events/hotcloud10/tech/full_papers/Zaharia.pdf)
> Abstarct - MapReduce and its variants have been highly successful in implementing large-scale data-intensive applications on commodity clusters. However, most of these systems are built around an acyclic data flow model that is not suitable for other popular applications. This paper focuses on one such class of applications: those that reuse a working set of data across multiple parallel operations. This includes many iterative machine learning algorithms, as well as interactive data analysis tools. We propose a new framework called Spark that supports these applications while retaining the scalability and fault tolerance of MapReduce. To achieve these goals, Spark introduces an abstraction called resilient distributed datasets (RDDs). An RDD is a read-only collection of objects partitioned across a set of machines that can be rebuilt if a partition is lost. Spark can outperform Hadoop by 10x in iterative machine learning jobs, and can be used to interactively query a 39 GB dataset with sub-second response time.

20. [An Architecture for Fast and General Data Processing on Large Clusters - Phd thesis](https://www2.eecs.berkeley.edu/Pubs/TechRpts/2014/EECS-2014-12.pdf)

21. [The big data ecosystem at LinkedIn](https://dl.acm.org/citation.cfm?id=2463707)
> Abstarct - The use of large-scale data mining and machine learning has proliferated through the adoption of technologies such as Hadoop, with its simple programming semantics and rich and active ecosystem. This paper presents LinkedIn's Hadoop-based analytics stack, which allows data scientists and machine learning researchers to extract insights and build product features from massive amounts of data. In particular, we present our solutions to the ``last mile'' issues in providing a rich developer ecosystem. This includes easy ingress from and egress to online systems, and managing workflows as production processes. A key characteristic of our solution is that these distributed system concerns are completely abstracted away from researchers. For example, deploying data back into the online system is simply a 1-line Pig command that a data scientist can add to the end of their script. We also present case studies on how this ecosystem is used to solve problems ranging from recommendations to news feed updates to email digesting to descriptive analytical dashboards for our members.

22. [SAMOA: a platform for mining big data streams](https://dl.acm.org/citation.cfm?id=2488042)
> Abstarct - Social media and user generated content are causing an ever growing data deluge. The rate at which we produce data is growing steadily, thus creating larger and larger streams of continuously evolving data. Online news, micro-blogs, search queries are just a few examples of these continuous streams of user activities. The value of these streams relies in their freshness and relatedness to ongoing events. However, current (de-facto standard) solutions for big data analysis are not designed to deal with evolving streams. In this talk, we offer a sneak preview of SAMOA, an upcoming platform for mining dig data streams. SAMOA is a platform for online mining in a cluster/cloud environment. It features a pluggable architecture that allows it to run on several distributed stream processing engines such as S4 and Storm. SAMOA includes algorithms for the most common machine learning tasks such as classification and clustering. Finally, SAMOA will soon be open sourced in order to foster collaboration and research on big data stream mining.

23. [Drizzle: Fast and Adaptable Stream Processing at Scale](http://shivaram.org/drafts/drizzle.pdf)
> Abstarct - Large scale streaming systems aim to provide high throughput and low latency. They are often used to run mission-critical applications, and must be available 24×7. As such, these systems need to adapt in the face of the inherent changes in the workloads and failures, and do so with minimal impact on latency. Unfortunately, existing solutions require operators to choose between achieving low latency during normal operation and incurring minimal impact during adaptation. Record-at-a-time streaming systems, such as Naiad and Flink, provide low latency during normal execution but high latency during adaptation (e.g., recovery), while micro-batch systems, such as SparkStreaming and FlumeJava, adapt rapidly at the cost of high latency during normal operations. We propose Drizzle, a hybrid streaming system that unifies the benefits from both models to provide both low latency during normal operation and during adaptation. Our key observation is that while streaming workloads require millisecond-level execution, workload and cluster properties change less frequently. Based on this insight, Drizzle decouples execution granularity from coordination granularity. Our experiments on a 128 node EC2 cluster show that Drizzle can achieve end-to-end record processing latencies of less than 100ms and can get up to 3.5x lower latency than Spark. Compared to Flink, a record-at-a-time streaming system, we show that Drizzle can recover around 4x faster from failures and that Drizzle has up to 13x lower latency during recovery.

24. [GraphX: Graph Processing in a Distributed Dataflow Framework](https://www.usenix.org/system/files/conference/osdi14/osdi14-paper-gonzalez.pdf)
> Abstarct - In pursuit of graph processing performance, the systems community has largely abandoned general-purpose distributed dataflow frameworks in favor of specialized graph processing systems that provide tailored programming abstractions and accelerate the execution of iterative graph algorithms. In this paper we argue that many of the advantages of specialized graph processing systems can be recovered in a modern general-purpose distributed dataflow system. We introduce GraphX, an embedded graph processing framework built on top of Apache Spark, a widely used distributed dataflow system. GraphX presents a familiar composable graph abstraction that is sufficient to express existing graph APIs, yet can be implemented using only a few basic dataflow operators (e.g., join, map, group-by). To achieve performance parity with specialized graph systems, GraphX recasts graph-specific optimizations as distributed join optimizations and materialized view maintenance. By leveraging advances in distributed dataflow frameworks, GraphX brings low-cost fault tolerance to graph processing. We evaluate GraphX on real workloads and demonstrate that GraphX achieves an order of magnitude performance gain over the base dataflow framework and matches the performance of specialized graph processing systems while enabling a wider range of computation.

25. [State Management in Apache Flink](http://www.vldb.org/pvldb/vol10/p1718-carbone.pdf)
> Abstarct - Stream processors are emerging in industry as an apparatus that drives analytical but also mission critical services handling the core of persistent application logic. Thus, apart from scalability and low-latency, a rising system need is first-class support for application state together with strong consistency guarantees, and adaptivity to cluster reconfigurations, software patches and partial failures. Although prior systems research has addressed some of these specific problems, the practical challenge lies on how such guarantees can be materialized in a transparent, non-intrusive manner that relieves the user from unnecessary constraints. Such needs served as the main design principles of state management in Apache Flink, an open source, scalable stream processor. We present Flink’s core pipelined, in-flight mechanism which guarantees the creation of lightweight, consistent, distributed snapshots of application state, progressively, without impacting continuous execution. Consistent snapshots cover all needs for system reconfiguration, fault tolerance and version management through coarse grained rollback recovery. Application state is declared explicitly to the system, allowing efficient partitioning and transparent commits to persistent storage. We further present Flink’s backend implementations and mechanisms for high availability, external state queries and output commit. Finally, we demonstrate how these mechanisms behave in practice with metrics and largedeployment insights exhibiting the low performance trade-offs of our approach and the general benefits of exploiting asynchrony in continuous, yet sustainable system deployments.

26. [HAMA: An Efficient Matrix Computation with the MapReduce Framework](https://pdfs.semanticscholar.org/55b2/97c1c69a1721a03018b9d1bd88e8807ed12e.pdf)
> Abstract - Various scientific computations have become so complex, and thus computation tools play an important role. In this paper, we explore the state-of-the-art framework providing highlevel matrix computation primitives with MapReduce through the case study approach, and demonstrate these primitives with different computation engines to show the performance and scalability. We believe the opportunity for using MapReduce in scientific computation is even more promising than the success to date in the parallel systems literature.

27. [Big Data Frameworks: A Comparative Study](https://www.researchgate.net/publication/309572509_Big_Data_Frameworks_A_Comparative_Study)
> Abstract - Recently, increasingly large amounts of data are generated from a variety of sources. Existing data processing technologies are not suitable to cope with the huge amounts of generated data. Yet, many research works focus on Big Data, a buzzword referring to the processing of massive volumes of (unstructured) data. Recently proposed frameworks for Big Data applications help to store, analyze and process the data. In this paper, we discuss the challenges of Big Data and we survey existing Big Data frameworks. We also present an experimental evaluation and a comparative study of the most popular Big Data frameworks. This survey is concluded with a presentation of best practices related to the use of studied frameworks in several application domains such as machine learning, graph processing and real-world applications

28. [A Survey of State Management in Big Data Processing Systems](https://arxiv.org/pdf/1702.01596.pdf)
> Abstract - State management and its use in diverse applications varies widely across big data processing systems. This is evident in both the research literature and existing systems, such as Apache Flink, Apache Samza, Apache Spark, and Apache Storm. Given the pivotal role that state management plays in various use cases, in this survey, we present some of the most important uses of state as an enabler, discuss the alternative approaches used to handle and implement state, propose a taxonomy to capture the many facets of state management, and highlight new research directions. Our aim is to provide insight into disparate state management techniques, motivate others to pursue research in this area, and draw attention to some open problems.

29. [Reliability-Aware Approach: An Incremental Checkpoint/Restart Model in HPC Environments](https://www.researchgate.net/publication/4340819_Reliability-Aware_Approach_An_Incremental_CheckpointRestart_Model_in_HPC_Environments)
> Abstract - For full checkpoint on a large-scale HPC system, huge memory contexts must potentially be transferred through the network and saved in a reliable storage. As such, the time taken to checkpoint becomes a critical issue which directly impacts the total execution time. Therefore, incremental checkpoint as a less intrusive method to reduce the waste time has been gaining significant attentions in the HPC community. In this paper, we built a model that aims to reduce full checkpoint overhead by performing a set of incremental checkpoints between two consecutive full checkpoints. Moreover, a method to find the number of those incremental checkpoints is given. Furthermore, most of the comparison results between the incremental checkpoint model and the full checkpoint model (Liu et al., 2007) on the same failure data set show that the total waste time in the incremental checkpoint model is significantly smaller than the waste time in the full checkpoint model.

30. [Monolith: Real Time Recommendation System With Collisionless Embedding Table](https://arxiv.org/pdf/2209.07663)
> Abstract - Building a scalable and real-time recommendation system is vital for many businesses driven by time-sensitive customer feedback, such as short-videos ranking or online ads. Despite the ubiquitous adoption of production scale deep learning frameworks like TensorFlow or PyTorch, these general-purpose frameworks fall short of business demands in recommendation scenarios for various reasons: on one hand, tweaking systems based on static parameters and dense computations for recommendation with dynamic and sparse features is detrimental to model quality; on the other hand, such frameworks are designed with batch-training stage and serving stage completely separated, preventing the model from interacting with customer feedback in real-time. These issues led us to reexamine traditional approaches and explore radically different design choices. In this paper, we present Monolith, a system tailored for online training. Our design has been driven by observations of our application workloads and production environment that reflects a marked departure from other recommendations systems. Our contributions are manifold: first, we crafted a collisionless embedding table with optimizations such as expirable embeddings and frequency filtering to reduce its memory footprint; second, we provide an production-ready online training architecture with high fault-tolerance; finally, we proved that system reliability could be traded-off for real-time learning. Monolith has successfully landed in the BytePlus Recommend product.

31. [Spanner: Google’s Globally-Distributed Database](https://static.googleusercontent.com/media/research.google.com/en//archive/spanner-osdi2012.pdf)
> Abstract - Spanner is Google’s scalable, multi-version, globallydistributed, and synchronously-replicated database. It is the first system to distribute data at global scale and support externally-consistent distributed transactions. This paper describes how Spanner is structured, its feature set, the rationale underlying various design decisions, and a novel time API that exposes clock uncertainty. This API and its implementation are critical to supporting external consistency and a variety of powerful features: nonblocking reads in the past, lock-free read-only transactions, and atomic schema changes, across all of Spanner
