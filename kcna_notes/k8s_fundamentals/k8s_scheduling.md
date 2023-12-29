# Scheduling

## **Scheduling in Kubernetes**

- **Definition and Evolution of Scheduling:**
    - **Basic Concept:**
        - Scheduling is a sub-category of container orchestration.
        - Describes the automated process of selecting the appropriate worker node to run a containerized workload.
    - **Historical Perspective:**
        - In the past, scheduling was a manual task for system administrators.
        - Involved choosing the right server for an application based on available servers, capacity, and other properties.
- **Kubernetes Scheduling Components:**
    - **kube-scheduler:**
        - In a Kubernetes cluster, kube-scheduler is responsible for making scheduling decisions.
        - Initiates the scheduling process when a new Pod object is created.
- **Declarative Approach in Kubernetes:**
    - **Process:**
        - Kubernetes uses a declarative approach.
        - The Pod is described first, and then the scheduler selects a node where the Pod will be started by the kubelet and the container runtime.
- **User Input in Scheduling:**
    - **Misconception:**
        - Commonly misunderstood that Kubernetes uses artificial intelligence for workload analysis and dynamic Pod movement based on various factors.
        - **Reality:**
            - Users need to provide information about application requirements.
            - Includes CPU and memory requests, as well as node-specific properties.
- **User-Specified Requirements:**
    - **Example:**
        - Users can request specific resources such as two CPU cores, four gigabytes of memory, and express preferences for node properties (e.g., fast disks).
- **Scheduling Decision Process:**
    - **Filtering Nodes:**
        - The scheduler filters nodes that meet specified requirements.
    - **Priority:**
        - If multiple nodes meet requirements equally, the scheduler prioritizes the node with the fewest Pods.
    - **Default Behavior:**
        - If no additional requirements are specified, the default behavior is to schedule the Pod on the node with the least number of Pods.
- **Handling Insufficient Resources:**
    - **Retry Mechanism:**
        - If the desired state cannot be established (e.g., insufficient resources on worker nodes), the scheduler retries until an appropriate node is found.

### [Kubernetes Fundamentals](https://kevinsulatra.github.io/k8snotes/kcna_notes/k8s_fundamentals/k8s_fundamentals.html)
