# **Container Orchestration Fundamentals**

- **Challenges in Container Operations:**
    - Running containers locally or on a single server is straightforward, but operational challenges arise with widespread container usage.
    - The high efficiency of containers results in smaller applications and services, leading to an abundance of loosely coupled, isolated, and independent containers.
- **Microservice Architectures:**
    - Small, self-contained containers form the basis of microservice architectures.
    - These containers encapsulate discrete units of business logic within a larger application.
- **Managing Large Container Deployments:**
    - Deploying and managing numerous containers requires a system for efficient management.
    - Challenges include providing compute resources, scheduling, resource allocation, availability management, failover, scaling, networking, and storage provisioning.
- **Container Orchestration Systems:**
    - Container orchestration systems address the need for managing large container deployments.
    - Comprising a control plane for container management and worker nodes for container hosting.
- **Key Orchestration System Responsibilities:**
    - Provide compute resources (virtual machines) for container execution.
    - Schedule containers efficiently across servers.
    - Allocate CPU and memory resources to containers.
    - Manage container availability and replace failed instances.
    - Scale containers in response to increased load.
    - Establish networking to connect containers.
    - Provision storage for containers requiring persistent data.
- **Industry Standard:**
    - Kubernetes has emerged as the industry-standard container orchestration system.
    - Chosen for its effectiveness in addressing the complexities of container management.
    - Other systems, once relevant, have faded in significance over the years.

### [**Container Orchestration**](https://kevinsulatra.github.io/k8snotes/kcna_notes/container_orchestration/container_orchestration.html)
