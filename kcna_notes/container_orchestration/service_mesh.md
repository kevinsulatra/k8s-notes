# **Service Mesh**

- **Complexity of Microservices Networking:**
    - Networking in microservices and containers can become complex and opaque for developers and administrators.
    - Desire for additional functionalities such as monitoring, access control, and encryption of networking traffic.
- **Proxy Servers to Manage Network Traffic:**
    - Instead of integrating complex networking functionalities into applications, using a separate container with this functionality is a common approach.
    - Software managing network traffic is known as a proxy (e.g., nginx, haproxy, envoy).
- **Service Mesh Concept:**
    - Extending the proxy idea, a service mesh involves adding a proxy server to every container in the architecture.
    - Proxies handle network communication between services.
    - Examples of service meshes: istio and linkerd.
- **Simplified Encryption with Service Mesh:**
    - Example: Achieving encryption between applications typically involves configuring libraries, managing digital certificates, etc.
    - In a service mesh, traffic between applications is routed through proxies, simplifying encryption implementation.
- **Data Plane and Control Plane in Service Mesh:**
    - Proxies in the service mesh form the data plane, where networking rules are implemented to shape traffic flow.
    - The control plane centrally manages these rules, defining how traffic flows between services and specifying proxy configurations.
- **Configuration vs. Code Implementation:**
    - Instead of writing code and installing libraries, a config file is used in a service mesh.
    - Configuration file specifies rules like encrypted communication between specific services.
    - Config uploaded to the control plane, distributed to the data plane to enforce the defined rules.
- **Evolution of Service Mesh Terminology:**
    - Initially, the term "service mesh" described a basic idea of handling traffic in container platforms with proxies.
    - The Service Mesh Interface (SMI) project aims to standardize the implementation of service meshes from various providers.
    - Focus on Kubernetes, standardizing the end-user experience and integration with Kubernetes providers.
    - Current [specification](https://github.com/servicemeshinterface/smi-spec) available on GitHub.

    ![Istio Mesh](../images/istio_mesh.png)
    **Istio Architecture**, retrieved from [istio.io](https://istio.io/v1.10/docs/ops/deployment/architecture/)

### [**Container Orchestration**](https://kevinsulatra.github.io/k8snotes/kcna_notes/container_orchestration/container_orchestration.html)
