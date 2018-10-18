Rise of Cloud-Native
  What do these innovative companies have in common?
  * Speed of innovation
  * Always-available services
  * Web scale
  * Mobile-centric user experiences
  
 By cloud, we mean any computing environment in which computing, networking, 
 and storage resources can be provisioned and released elastically in an on-demand, 
 self-service manner.
 
 Why Cloud-Native Application Architectures?
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
    In the context of twelve-factor, application (or app) refers to a single
    deployable unit. Organizations will often refer to multiple collaborating
    deployables as an application. In this context, however, we will
    refer to these multiple collaborating deployables as a distributed system.
* Microservices
* Self-Service Agile Infrastructure
* API-Based Collaboration
* Antifragility
 
