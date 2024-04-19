## **Cloud Computing:**

- **Definition:** It’s the delivery of IT resources over the internet. You can access services like storage, computing, networking, security, and infrastructure from a cloud provider.
- **Features:** Includes broad network access, resource integration, and on-demand self-service.
- **Advantages:** Cost-saving, high-speed, reliability, mobility, and unlimited storage capacity.
- **Disadvantages:** Performance can vary, technical issues, security threat, dependency on internet connectivity, and limited control.

## Cloud deployment models:

**Public Cloud:**
- **Definition:** Public Cloud is a type of cloud computing where the infrastructure and services are owned and operated by a third-party provider and made available to the public over the internet².
- **Features:** Accessible from anywhere, automatic software updates, pay for what you use².
- **Advantages:** Cost-efficient, automatic software updates, accessibility².
- **Disadvantages:** Security and privacy concerns, limited control, reliance on internet connectivity, service downtime, compliance and regulatory issues, cost overruns².

**Private Cloud:**
- **Definition:** Private Cloud is a type of cloud computing that provides similar advantages to the public cloud but through a proprietary architecture².
- **Features:** Increased control and security³.
- **Advantages:** Control, security³.
- **Disadvantages:** More costly, less scalable³.

**Hybrid Cloud:**
- **Definition:** Hybrid Cloud is a type of cloud computing that combines on-premises infrastructure or a private cloud with a public cloud¹. It allows data and apps to move between the two environments¹.
- **Features:** Combines the benefits of public and private cloud environments⁵.
- **Advantages:** Control, flexibility, cost-effectiveness, ease of transition¹.
- **Disadvantages:** Requires specialized expertise to manage effectively³.

## Cloud Reference Model

**IaaS (Infrastructure as a Service):**
- **Definition:** IaaS delivers on-demand infrastructure resources to organizations via the cloud, such as compute, storage, networking, and virtualization².
- **Features:** Users don't have to manage, maintain, or update their own data center infrastructure, but are responsible for the operating system, middleware, virtual machines, and any apps or data².
- **Advantages:** Users don't have to manage their own data center infrastructure².
- **Disadvantages:** Users are responsible for the operating system, middleware, virtual machines, and any apps or data².

**PaaS (Platform as a Service):**
- **Definition:** PaaS provides a framework for creating and deploying applications while removing the need for infrastructure management³.
- **Features:** Many PaaS providers let developers choose the services they need and leave out the rest, which allows them to integrate more resources as needed or scale back the services they no longer want to use⁴.
- **Advantages:** It's scalable⁴.
- **Disadvantages:** There's no back-end to think about⁴.

**SaaS (Software as a Service):**
- **Definition:** The main advantage of SaaS-based software models is the ability to obtain specific functionalities of all types of software without the need to install and run any application locally⁵.
- **Features:** Allows access from any operating system, device, or physical location with the only requirement being the need for an internet connection⁵.
- **Advantages:** No need to install and run any application locally⁵.
- **Disadvantages:** Requires an internet connection⁵.

## Mainframe vs Cloud Computing

**Mainframe:**
- **Definition:** Mainframes are powerful, centralized computers for handling large-scale transaction processing and data-intensive workloads¹.
- **Features:** Mainframes offer robust security, reliability, and scalability. They excel in handling mission-critical workloads and provide high availability¹.
- **Advantages:** Mainframes offer robust processing power and data security¹.
- **Disadvantages:** Mainframes can be expensive to acquire and maintain. They require specialized expertise and infrastructure. Upgrading and scaling mainframe systems can be complex and time-consuming¹.

**Cloud Computing:**
- **Definition:** Cloud computing is a technology that delivers on-demand services over the Internet, providing users with scalable and flexible solutions¹.
- **Features:** Cloud computing offers flexibility, scalability, and cost-efficiency¹.
- **Advantages:** Cloud computing provides scalability, flexibility, and cost-effectiveness¹.
- **Disadvantages:** Cloud computing may face concerns regarding data privacy and security. It also requires internet connectivity¹.

## Parallel vs Distributed Computing

**Parallel Computing:**
- **Definition:** Parallel computing involves multiple processors performing multiple tasks simultaneously¹².
- **Features:** It can either have shared or distributed memory. Processors communicate with each other through a bus².
- **Advantages:** It provides concurrency, saves time and money, and improves system performance¹².
- **Disadvantages:** The multi-core architectures consume a lot of power. Parallel solutions are more difficult to implement, debug, and prove right due to the complexity of communication and coordination¹.

**Distributed Computing:**
- **Definition:** Distributed computing involves multiple autonomous computers that operate as a single system¹². A single task is divided among different computers².
- **Features:** There is no shared memory and computers communicate with each other through message passing².
- **Advantages:** It improves system scalability, fault tolerance, and resource sharing capabilities².
- **Disadvantages:** Distributed computing has to be less bandwidth intensive⁴.

## Client-Server vs P2P

**Client-Server:**
- **Definition:** In a Client-Server network, clients and servers are differentiated. A centralized server is used to store the data and respond to the services requested by the client¹.
- **Features:** It focuses on information sharing. The server provides all the services and data while the clients request for services and data¹.
- **Advantages:** Client-Server networks are more stable and can be used for both small and large networks¹.
- **Disadvantages:** They are costlier than Peer-to-Peer networks and less stable if the number of peers increases¹.

**Peer-to-Peer (P2P):**
- **Definition:** In a Peer-to-Peer network, clients and servers are not differentiated. Each peer has its own data and can both request and respond to services¹.
- **Features:** It focuses on connectivity. All the members (peers) of the network act as the service providers and consumers¹.
- **Advantages:** P2P networks are less costly than Client-Server networks and are generally suited for small networks with fewer than 10 computers¹.
- **Disadvantages:** P2P networks are less stable if the number of peers increases¹.

## RPC vs RMI

**RPC (Remote Procedure Call):**
- **Definition:** RPC supports procedural programming. It's an IPC mechanism where the software allows processes to manage shared data in an environment where different processes are executing on separate systems¹.
- **Features:** RPC is a library and OS dependent platform. The parameters passed in RPC are ordinary or normal data¹.
- **Advantages:** RPC provides a high provision of ease of programming¹. It's development cost is huge¹.
- **Disadvantages:** RPC creates more overhead and is less efficient than RMI¹. It does not provide any security¹. There is a huge problem of versioning in RPC¹.

**RMI (Remote Method Invocation):**
- **Definition:** RMI supports object-oriented programming which is java’s feature. A thread is allowed to call the method on a remote object¹.
- **Features:** RMI is a java platform. In RMI, objects are passed as a parameter rather than ordinary data¹.
- **Advantages:** RMI is more efficient than RPC¹. It provides client level security¹. It's development cost is fair or reasonable¹.
- **Disadvantages:** There is low Provision of ease of programming in RMI¹. There is possible versioning using RDMI¹.

## Client Server Architecture

**Definition:**
Client-Server Architecture is a computing model where the server hosts, delivers, and manages most of the resources and services requested by the client¹. It's also known as the networking computing model or client-server network as all requests and services are delivered over a network¹.

**Features:**
- **Centralized System:** It consolidates resources on servers for greater control and security⁴.
- **Flexible Client Options:** Allows for flexible client options⁴.
- **Robust Network:** Relies on a robust network for scalability and efficiency⁴.

**Advantages:**
- **Cost-Efficient:** Needs less maintenance cost⁵.
- **Scalability:** The capacity of the Client/Servers can be changed separately⁵.
- **Centralized System:** Data is in one single place⁵.

**Disadvantages:**
- **Cost Implications:** There are cost implications⁴.
- **Data Recovery:** Data recovery is made possible⁵.

## 2-Tier and 3-Tier Architecture

Sure, here's a summary of 2-Tier (Client-Server) and 3-Tier (Presentation, Application Logic, Storage) Architectures:

**2-Tier (Client-Server) Architecture:**
- **Definition:** In a 2-Tier architecture, the client and server are differentiated. A centralized server is used to store the data and respond to the services requested by the client¹.
- **Features:** It focuses on information sharing. The server provides all the services and data while the clients request for services and data¹.
- **Advantages:** 2-Tier applications are advantageous because they are fast to implement and communication is faster³.
- **Disadvantages:** The business logic lives in the presentation tier, the data tier or both. In 2-Tier architecture the presentation tier - and therefore the end user - has direct access to the data tier, and the business logic is often limited¹.

**3-Tier (Presentation, Application Logic, Storage) Architecture:**
- **Definition:** 3-Tier architecture organizes applications into three logical and physical computing tiers: the presentation tier (user interface), the application tier (where data is processed), and the data tier (where application data is stored and managed)¹.
- **Features:** Each tier runs on its own infrastructure, each tier can be developed simultaneously by a separate development team. And can be updated or scaled as needed without impacting the other tiers¹.
- **Advantages:** 3-Tier architecture improves scalability and performance by allowing each tier to be scaled independently. It also improves security by isolating the data tier from the presentation and application tiers⁴.
- **Disadvantages:** It is more complex than the 2-Tier client-server computing model, because it is more difficult to build a 3-Tier application compared to a 2-Tier application⁵.

## Flynns Taxonomy

**Definition:**
Flynn's Taxonomy is a classification of computer architectures proposed by Michael J. Flynn in 1966⁴. It classifies computer architectures based on the number of instruction streams and data streams that can be processed simultaneously¹.

**Features:**
- **Single-instruction, single-data (SISD):** An SISD computing system is a uniprocessor machine which is capable of executing a single instruction, operating on a single data stream¹.
- **Single-instruction, multiple-data (SIMD):** An SIMD system is a multiprocessor machine capable of executing the same instruction on all the CPUs but operating on different data streams¹.
- **Multiple-instruction, single-data (MISD):** An MISD computing system is a multiprocessor machine capable of executing different instructions on different PEs but all of them operating on the same dataset¹.
- **Multiple-instruction, multiple-data (MIMD):** An MIMD system is a multiprocessor machine which is capable of executing multiple instructions on multiple data sets¹.

**Advantages:**
Flynn's Taxonomy itself does not have any inherent advantages. It is simply a classification scheme for computer architectures³.

**Disadvantages:**
The different types of computer architectures that fall under Flynn's Taxonomy have their own disadvantages. For example, SISD systems are limited by the rate at which the computer can transfer information internally¹. SIMD systems are well suited to scientific computing since they involve lots of vector and matrix operations¹. MISD systems are not useful in most of the applications¹. MIMD systems are more complex and require more resources¹.

## SOC and SOA

**SOC (Service Oriented Computing):**
- **Definition:** SOC is the computing paradigm that utilizes services as fundamental elements for developing applications/solutions. To build the service model, SOC relies on the Service Oriented Architecture (SOA), which is a way of reorganizing software applications and infrastructure into a set of interacting services³.
- **Features:** SOC provides separate tiers for composing and coordinating services and for managing services in an open marketplace by employing grid services³.
- **Advantages:** SOC provides methods for service encapsulation, service discovery, service composition, service reusability and service integration¹.
- **Disadvantages:** The basic SOA does not address overarching concerns such as management, service orchestration, service transaction management and coordination, security, and other concerns that apply to all components in a services architecture³.

**SOA (Service Oriented Architecture):**
- **Definition:** SOA is an architectural approach in which applications make use of services available in the network¹. It defines a way to make software components reusable using the interfaces¹.
- **Features:** SOA provides interoperability between the services¹. It facilitates QoS (Quality of Services) through service contract based on Service Level Agreement (SLA)¹.
- **Advantages:** SOA is highly reusable, making it an efficient way to integrate legacy systems⁴. It's scalable, reliable, and secure⁴.
- **Disadvantages:** Services aren’t hard-coded into applications. Instead, services are a published to a registry, and when an application wants to use a service, it asks the registry to find the latest version².

## Parallel vs Distributed Processing

**Parallel Processing:**
- **Definition:** Parallel processing is the use of two or more processors (cores, computers) in combination to solve a single problem². It is a type of computing architecture in which several processors execute or process an application or computation simultaneously².
- **Features:** Parallel processing breaks down complex problems into smaller, independent tasks that can be processed simultaneously². These tasks are distributed among multiple processing units, such as CPU cores or computer nodes, to achieve a substantial reduction in processing time².
- **Advantages:** Parallel processing can handle complex calculations and data-intensive operations much faster than sequential computing². It saves time and money because many resources working together cut down on time and costs¹.
- **Disadvantages:** The multi-core architectures consume a lot of power. Parallel solutions are more difficult to implement, debug, and prove right due to the complexity of communication and coordination¹.

**Distributed Processing:**
- **Definition:** Distributed processing comprises several software components that reside on different systems but operate as a single system¹. A distributed system's computers can be physically close together and linked by a local network or geographically distant and linked by a wide area network (WAN)¹.
- **Features:** In distributed computing, each processor has its own private memory (distributed memory). Information is exchanged by passing messages between the processors³.
- **Advantages:** Distributed computing enables several computers to communicate with one another and achieve a goal¹. It provides methods for service encapsulation, service discovery, service composition, service reusability and service integration¹.
- **Disadvantages:** Distributed computing has to be less bandwidth intensive³. Therefore, the tasks have to be fewer dependents⁴.

## WebServices and its features

**Definition:**
Web Services are a standardized method for propagating messages between client and server applications over the network¹. They are software modules intended to carry out a specific set of functions¹. Web services can be found and invoked over the network, and they deliver functionality to the client that invoked the web service¹.

**Features:**
- **XML-Based:** Web services use XML at data description and data transportation layers².
- **Loosely Coupled:** A client of a web service is not tied to the web service directly².
- **Coarse-Grained:** Object-oriented technologies such as Java expose their functions through individual methods².
- **Ability to be Synchronous or Asynchronous:** Synchronicity specifies the binding of the client to the execution of the function².
- **Supports Remote Procedure Calls (RPCs):** Web services allow consumers to invoke procedures, functions, and methods on remote objects using an XML-based protocol².

**Advantages:**
- **Interoperability:** The inherent interoperability that comes with using vendor, platform, and language independent XML technologies⁴.
- **Communication is Platform-Independent:** Client and server do not require common features in order for communication to work³.

**Disadvantages:**
- **Relies on Standardized Formats:** One of the disadvantages lies in these formats³.

## Challenges of Cloud Computing

1. **Data Security and Privacy:** Data security is a major concern when switching to cloud computing. User or organizational data stored in the cloud is critical and private. Even if the cloud service provider assures data integrity, it is your responsibility to carry out user authentication and authorization, identity management, data encryption, and access control¹.

2. **Cost Management:** Even as almost all cloud service providers have a “Pay As You Go” model, which reduces the overall cost of the resources being used, there are times when there are huge costs incurred to the enterprise using cloud computing¹.

3. **Multi-Cloud Environments:** Common cloud computing issues and challenges with multi-cloud environments are - configuration errors, lack of security patches, data governance, and no granularity².

4. **Lack of Resources/Expertise:** The lack of resources and expertise is another challenge in cloud computing³.

5. **Cybersecurity Issues:** Cybersecurity issues are one of the three challenges in cloud computing³.

6. **Governance:** Governance was one of the top challenges in cloud computing for organizations of all sizes⁵.

## Web 2.0 Features and Applications

**Web 2.0:**

- **Definition:** Web 2.0 refers to websites that emphasize user-generated content, ease of use, participatory culture, and interoperability². It's an improved version of the first worldwide web, characterized specifically by the change from static to dynamic or user-generated content and also the growth of social media¹.

- **Features:** Web 2.0 allows users to collectively classify and find dynamic information that flows two ways between site owner and site user by means of evaluation, comments, and reviews⁴. It provides free sorting of information, permits users to retrieve and classify the information collectively, and has dynamic content that is responsive to user input⁴.

- **Applications:** Examples of Web 2.0 applications include hosted services (Google Maps), Web applications (Google Docs, Flickr), Video sharing sites (YouTube), wikis (MediaWiki), blogs (WordPress), social networking (Facebook), folksonomies (Delicious), Microblogging (Twitter), podcasting (Podcast Alley) & content hosting services¹.

## Mainframe vs Cluster vs Grid Computing

**Mainframe Computing:**
- **Definition:** Mainframes are powerful, centralized computers for handling large-scale transaction processing and data-intensive workloads³. They are designed to be reliable, secure, and capable of managing and processing vast amounts of data³.
- **Features:** Mainframes offer robust security, reliability, and scalability. They excel in handling mission-critical workloads and provide high availability³.
- **Advantages:** Mainframes offer robust processing power and data security³. They are also known for their high uptime, meaning they rarely go down or fail³.
- **Disadvantages:** Mainframes can be expensive to acquire and maintain. They require specialized expertise and infrastructure. Upgrading and scaling mainframe systems can be complex and time-consuming³.

**Cluster Computing:**
- **Definition:** A Computer Cluster is a local network of two or more homogeneous computers. A computation process on such a computer network i.e. cluster is called Cluster Computing¹.
- **Features:** Computers in a cluster are dedicated to the same work and perform no other task¹. Computers are located close to each other and are connected by a high-speed local area network bus¹.
- **Advantages:** High resource availability. If a single component in a computer cluster fails, the other machines process data without interruption³.
- **Disadvantages:** Cluster computing came as an alternative to mainframe technology. Each machine in the cluster was connected to each other by a network with high bandwidth. These were way cheaper than those mainframe systems⁴.

**Grid Computing:**
- **Definition:** Grid Computing can be defined as a network of homogeneous or heterogeneous computers working together over a long distance to perform a task that would rather be difficult for a single machine¹.
- **Features:** Computers in a grid contribute their unused processing resources to the grid computing network¹. Computers may be located at a huge distance from one another and are connected using a low-speed bus or the internet¹.
- **Advantages:** Grid computing solves complicated tasks, but cloud computing provides users access to some particular services at a low cost².
- **Disadvantages:** Grid computing contains a large number of servers and computers. Moreover, each of them executes independently².

## Data Parallelism vs Task Parallelism 

**Data Parallelism:**
- **Definition:** Data Parallelism means concurrent execution of the same task on each multiple computing core¹. It focuses on distributing the data across different nodes, which operate on the data in parallel².
- **Features:** Data Parallelism can be applied on regular data structures like arrays and matrices by working on each element in parallel². It involves running the same task on different subsets of the same data¹.
- **Advantages:** As there is only one execution thread operating on all sets of data, so the speedup is more¹. It is designed for optimum load balance on multiprocessor system¹.
- **Disadvantages:** The locality of data references plays an important part in evaluating the performance of a data parallel programming model².

**Task Parallelism:**
- **Definition:** Task Parallelism means concurrent execution of the different task on multiple computing cores¹. It involves running many different tasks at the same time on the same data⁴.
- **Features:** Different tasks are performed on the same or different data¹. Asynchronous computation is performed¹.
- **Advantages:** Task parallelism is the simultaneous execution on multiple cores of many different functions across the same or different datasets³.
- **Disadvantages:** As each processor will execute a different thread or process on the same or different set of data, so speedup is less¹.

## Components of Distributed system

**Distributed System:**

- **Definition:** A Distributed System is a collection of autonomous computer systems that are physically separated but are connected by a centralized computer network that is equipped with distributed system software². The autonomous computers communicate among each system by sharing resources and files and performing the tasks assigned to them².

- **Components:**
    - **Autonomous Systems:** These are the individual computer systems that are part of the distributed system².
    - **Centralized Network:** This is the network that connects the autonomous systems².
    - **Distributed System Software:** This software enables computers to coordinate their activities and to share the resources such as hardware, software, data, etc².
    - **Database:** It is used to store the processed data that are processed by each node/system of the distributed systems that are connected to the centralized network².
    - **Middleware Services:** Middleware services enable some services which are not present in the local systems or centralized system default by acting as an interface between the centralized system and the local systems².

- **Advantages:**
    - **Better Performance:** By using the resources of numerous computers to tackle the workload, distributed systems can perform at higher levels than centralized systems¹.
    - **Cost Effectivity:** Although distributed systems consist of high implementation costs, they are relatively cost-effective in the long run¹.
    - **Efficiency:** Distributed systems are made to be efficient in every aspect since they possess multiple computers¹.
    - **Scalability:** Distributed systems are made on default to be scalable¹.
    - **Reliability:** Distributed systems are far more reliable than single systems in terms of failures¹.
    - **Geographic Distribution:** Geographic distribution is a feature of distributed systems that enables them to offer services to users in various areas¹.
    - **Reduced Cost:** Because distributed systems can make use of existing resources rather than needing to buy new gear, they can be less expensive than centralized systems¹.

- **Disadvantages:**
    - **Compatibility:** In a distributed system, compatibility across multiple nodes and software systems can be a problem since they may employ various hardware, software, or protocols¹.
    - **Startup Cost:** Compared to a single system, the implementation cost of a distributed system is significantly higher¹.
    - **Single Point of Failure:** If the main system fails, it will affect the whole system³.
    - **Programming Complexity:** The process of designing and creating distributed systems is difficult and fraught with difficulties¹.