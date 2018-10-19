# Rise of Cloud-Native
  What do these innovative companies have in common?
  * Speed of innovation
  * Always-available services
  * Web scale
  * Mobile-centric user experiences
  
 By cloud, we mean any computing environment in which computing, networking, 
 and storage resources can be provisioned and released elastically in an on-demand, 
 self-service manner.
 
 ## Why Cloud-Native Application Architectures?
 * Speed - Businesses that are able to innovate, experiment, and deliver software-based 
 solutions quickly are outcompeting those that follow more traditional delivery models.
 Why are frequent deployments impor tant? 
 If you can deploy hundreds of times per day, you can recover from mistakes almost instantly. 
 If you can recover from mistakes almost instantly, you can take on more risk. 
 If you can take on more risk, you can try wild experiments—the results might turn
 into your next competitive advantage.
 
 * Safety - Cloud-native application architectures balance the need to move rapidly with the
needs of stability, availability, and durability.
    So how do we go fast and safe?
      Visibility - We need the ability to measure everything, 
        establish a profile for “what’s normal,” detect deviations from the norm 
        (including absolute values and rate of change), 
        and identify the components contributing to those deviations.
     Fault isolation - Need to limit the scope of components or features that could be 
        affected by a failure.
     Fault tolerance - Prevent a failure in one of those components from 
        causing a cascading failure across its possibly many transitive dependencies.
     Automated recovery - With visibility, fault isolation, and fault tolerance, 
        we have the tools we need to identify failure, recover from failure, 
        and provide a reasonable level of service to our customers while we’re
        engaging in the process of identification and recovery.

 * Scale - Applications must be architected differently for horizontal rather than vertical
    scale. The elasticity of the cloud demands ephemerality. Not only
    must we be able to create new application instances quickly; we
    must also be able to dispose of them quickly and safely. This need is
    a question of state management: how does the disposable interact
    with the persistent? Application need to be stateless and externalize state to in-memory data grids, caches, 
    and persistent object stores,
    
* Client Diversity - Huge diversity in mobile platforms has also placed demands on
    application architectures.Cloud-native application architectures also support the 
    notion of mobile-first development through design patterns such as the API Gateway, 
    which transfers the burden of service aggregation back to the server-side.
      
Defining Cloud-Native Architectures
* Twelve-Factor Applications - https://12factor.net/

    The patterns describe an application archetype that optimizes for the
    “why” of cloud-native application architectures. They focus on speed, safety, and scale 
    by emphasizing declarative configuration, stateless/shared-nothing processes 
    that horizontally scale, and an overall loose coupling to the deployment environment. 
     
    In the context of twelve-factor, application (or app) refers to a single
    deployable unit. Organizations will often refer to multiple collaborating
    deployables as an application. In this context, however, we will
    refer to these multiple collaborating deployables as a distributed system.
* Microservices
  Microservices represent the decomposition of monolithic business systems into independently deployable services that do “one thing well.” That one thing usually represents a business capability, or the smallest, “atomic” unit of service that delivers business value.
  
* Self-Service Agile Infrastructure
  Teams developing cloud-native application architectures are typically responsible 
  for their deployment and ongoing operations. Successful adopters of cloud-native
  applications have empowered teams with self-service platforms.
  Contract compliance can be verified on both sides of a service-to-service interaction 
  via consumer-driven contracts. 
  
* API-Based Collaboration
  The sole mode of interaction between services in a cloud-native application architecture is via published and versioned APIs. 
  
* Antifragility
  The quality of a system that gets stronger when subjected to stressors. 
  Can we build architectures that way? Adopters of cloud-native architectures have sought to build them. One example is the Netflix Simian Army project, with the famous submodule “Chaos Monkey,” which injects random failures into production components with the goal of identifying and eliminating weaknesses in the architecture. 
 
## Changes Needed
Reduce waste.
Lean principles translates easily in sw dev.
This will help orgs embrace the cultural and organizational transformations that revolve 
around eliminating structures, processes, and activities that create waste.

### Cultural Change
* From Silos to DevOps
     Development’s mission is usually viewed as delivering additional value to the organization through the development of software features. These features, by their very nature, introduce change into the IT ecosystem. So development’s mission can be described as “delivering change,” and is very often incentivized around how much change it delivers.
     IT operations is usually tasked with maintaining the desired levels of availability, resiliency, performance, and durability of IT systems. Therefore they are very often incentivized to maintain key perfomance indicators (KPIs) such as mean time between failures (MTBF) and mean time to recovery (MTTR).
     DevOps represents the idea of tearing down these silos and building shared toolsets, vocabularies, and communication structures in service of a culture focused on a single goal: delivering value rapidly and safely. 
     Incentive structures are then created that reinforce and award behaviors that lead the organization in the direction of that goal.
     
* From Punctuated Equilibrium to Continuous Delivery     
    Rather than punctuated equilibrium driven by a waterscrumfall organization, we embrace the principles of value from end to end. A useful model for envisioning such a lifecycle is the idea of “Concept to Cash” described by Mary and Tom Poppendieck in their book Implementing Lean Software Development (Addison-Wesley). This approach considers all of the activities necessary to carry a business idea from its conception to the point where it generates profit, and constructs a value stream aligning people and process toward the optimal achievement of that goal.
    
* Centralized Governance to Decentralized Autonomy
    Architectural committees often only assemble periodically, and long waiting queues of work often ensue. Even small data model changes—changes that could be implemented in minutes or hours, and that would be readily approved by the committee—lay wasting in an ever-growing stack of to-do items.
    The teams building cloud-native applications (“Business Capability Teams”) own all facets of the capability they’re charged with delivering. They own and govern the data, the technology stack, the application architecture, the design of individual components, and the API contract delivered to the remainder of the organization. If a decision needs to be made, it’s made and executed upon autonomously by the team.The decentralization and autonomy of individual teams is balanced by minimal, lightweight structures that are imposed on the integration patterns used between independently developed and deployed services (e.g., they prefer HTTP REST JSON APIs rather than many different styles of RPC). 

### Organizational Change
The theory behind this reorganization is the famous observation known as Conway’s Law. Our solution is to create a team combining staff with many disciplines around each long-term product, instead of segregating staff that have a single discipline in each own team, such as testing.

* Business Capability Teams
    

    Any organization that designs a system (defined broadly) will produce a design whose structure is a copy of the organization’s communication structure. - Melvyn Conway
    
    Try https://www.thoughtworks.com/radar/techniques/inverse-conway-maneuver
    Rather than building an architecture that matches their org chart, they determine the architecture they want and restructure their organization to match that architecture. If you do that, according to Conway, the architecture that you desire will eventually emerge.
    Teams are organized as cross-functional, business capability teams that develop products rather than projects. Products are long-lived efforts that continue until they no longer provide value to the business.
    If we follow the Inverse Conway Maneuver, we’ll start with the domain model for the organization, and seek to identify business capabilities that can be encapsulated within bounded contexts (which we’ll cover in “Decomposing Data”). Once we identify these capabilities, we create business capability teams to own them throughout their useful lifecycle. Business capability teams own the entire development-to-operations lifecycle for their applications.
    
### The Platform Operations Team
    
   Owns self-service agile infrastructure.
   This team typically includes the traditional system, network, and storage administrator roles.
   Rather than queuing up requests for application environments and data services to be provisioned, business capability teams are able to take the leaner approach of building automated release pipelines that provision environments and services on-demand.

### Technical Change

   * Decomposing Monoliths
      Traditional n-tier, monolithic enterprise applications rarely operate well when deployed to cloud infrastructure and they are not very compatible with the idea of elastic and ephemeral infrastructure.
      
   * Decomposing Data
      If business capability teams are supposedly autonomous but are forced to collaborate via a single data store, the monolithic barrier to innovation is simply relocated.
      Our success is largely governed by the quality of our domain model (and the ubiquitous language that underpins it). For a domain model to be effective, it must also be internally consistent—we should not find terms or concepts with inconsistent definitions within the same model.
      Bounded contexts allow you to keep inconsistent definitions of a single concept across the organization, as long as they are defined consistently within the contexts themselves.
      We define our bounded contexts, assign them a set of business capabilities, commission capability teams to own those business capabilities, and have them build twelve-factor applications. The fact that these applications are independently deployable provides business capability teams with a useful set of technical tools for operation.
      Decomposition allows for the application of polyglot persistence, or choosing different data stores based on data shape and read/write access patterns. However, data must often be recomposed via event-driven techniques in order to ask cross-context questions. Techniques such as command query responsibility segregation (CQRS) and event sourcing, beyond the scope of this report, are often helpful when synchronizing similar concepts across contexts.
      IMPOTANT : Twelve-factor is primarily a technical specification, whereas microservices are primarily a business specification. 
      
* Containerization
    Containers leverage modern Linux kernel primitives such as control groups (cgroups) and namespaces to provide similar resource allocation and isolation features as those provided by virtual machines with much less overhead and much greater portability.
    
* From Orchestration to Choreography
    Enterprise integration of services has traditionally been accomplished via the enterprise service bus (ESB). The ESB becomes the owner of all routing, transformation, policy, security, and other decisions governing the interaction between services. We call this orchestration, analogous to the conductor who determines the course of the music performed by an orchestra during its performance.
    
    Cloud-native architectures, such as microservices, tend to prefer choreography, akin to dancers in a ballet. Rather than placing the smarts in the integration mechanism, they are placed in the endpoints, akin to the dumb pipes and smart filters of the Unix architecture.Services adapt to changing circumstances in their environment via patterns such as client-side load balancing (“Routing and Load Balancing”) and circuit breakers (“Fault-Tolerance”).
    IMP : Choreography simply acknowledges and exposes the essential complexity of the system. 
    Teams are able to adapt to their changing circumstances without the difficult overhead of coordinating with other teams, and avoid the overhead of coordinating changes with a centrally-managed ESB.
    
All of these changes create autonomous units that are able to safely move at the desired rate of innovation.    
