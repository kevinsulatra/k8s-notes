# Networking

## **Kubernetes Networking Overview**

- **Complexity of Kubernetes Networking:**
    - Kubernetes networking can be intricate and challenging, with concepts extending beyond Kubernetes-specific aspects covered in the Container Orchestration chapter.
- **Four Kubernetes Networking Problems:**
    1. **Container-to-Container Communications:**
        - Addressed by the Pod concept, as detailed later.
    2. **Pod-to-Pod Communications:**
        - Resolved through an overlay network.
    3. **Pod-to-Service Communications:**
        - Implemented by kube-proxy and packet filter on the node.
    4. **External-to-Service Communications:**
        - Implemented by kube-proxy and packet filter on the node.
- **Three Key Networking Requirements:**
    1. All pods can communicate with each other across nodes.
    2. All nodes can communicate with all pods.
    3. No Network Address Translation (NAT).
- **Networking Implementation Options in Kubernetes:**
    - **Network Vendors:**
        1. Project Calico
        2. Weave
        3. Cilium
- **Automatic IP Address Assignment in Kubernetes:**
    - Every Pod in Kubernetes is assigned its own IP address without manual configuration.
    - CoreDNS, a DNS server add-on, is commonly included in Kubernetes setups for service discovery and name resolution within the cluster.
- **Network Policies in Kubernetes:**
    - **Control at IP and Port Level:**
        - If control over traffic flow at the IP address or port level is desired.
    - **Implementation:**
        - Network Policies act as cluster-internal firewalls.
        - Defined for a set of pods or a namespace using a selector to specify allowed traffic.
        - IP-based Network Policies use IP blocks (CIDR ranges).
    - **Implementation Responsibility:**
        - Network Policies are implemented by the network plugin.
        - Requires a networking solution supporting NetworkPolicy; creating a NetworkPolicy resource without a compatible controller has no effect.

### [Kubernetes Fundamentals](https://kevinsulatra.github.io/k8snotes/kcna_notes/k8s_fundamentals/k8s_fundamentals.html)
