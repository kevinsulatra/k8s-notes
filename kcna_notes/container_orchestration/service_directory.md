# **Service Discovery & DNS**

- **Traditional Server Management vs. Container Orchestration:**
    - In traditional data centers, server management was manageable, and administrators often remembered important IP addresses.
    - Maintained lists of servers, host names, IP addresses, and purposes were manually handled.
- **Challenges in Container Orchestration:**
    - Container orchestration introduces complexity:
        - Hundreds or thousands of containers with individual IP addresses.
        - Deployment on diverse hosts, data centers, or geolocations.
        - Containers or services require DNS for communication.
        - Dynamic removal of container information when deleted.
- **Automation as the Solution:**
    - Automation replaces manual maintenance of server/container lists.
    - Information centralized in a Service Registry.
    - Automation includes Service Discovery, enabling finding and requesting information about services in the network.
- **Key Challenges in Container Orchestration Platforms:**
    - Managing hundreds or thousands of containers with individual IP addresses.
    - Deploying containers across diverse hosts, data centers, or geolocations.
    - Necessity for DNS for effective communication between containers or services.
    - Dynamic removal of container information from the system when containers are deleted.

    ## Approaches to Service Discovery

    ### DNS

    Modern DNS servers that have a service API can be used to register new services as they are created. This approach is pretty straightforward, as most organizations already have DNS servers with the appropriate capabilities.

    ### Key-Value-Store

    Using a strongly consistent datastore especially to store 
    information about services. A lot of systems are able to operate highly 
    available with strong failover mechanisms. Popular choices, especially 
    for clustering, are [etcd](https://github.com/coreos/etcd/), [Consul](https://www.consul.io/) or [Apache Zookeeper](https://zookeeper.apache.org/).

### [**Container Orchestration**](https://kevinsulatra.github.io/k8snotes/kcna_notes/container_orchestration/container_orchestration.html)
