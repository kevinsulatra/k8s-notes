# Storage

- **Ephemeral Nature of Containers - Storage Perspective:**
    - Containers have a notable limitation from a storage perspective: they are ephemeral.
    - Ephemeral implies temporary or short-lived, highlighting a key characteristic of containers.
- **Container Image Structure:**
    - Container images are primarily read-only.
    - Comprise different layers, each capturing additions made during the build phase.
    - This structure ensures consistent behavior and functionality when starting containers from the image.
- **Read-Write Layer for File Writing:**
    - Many applications require writing files during execution.
    - To facilitate file writing, a read-write layer is added on top of the container image when a container is started from an image.
    - This read-write layer allows the temporary modification of the container's file system during its runtime.
![Container layers](../images/container_layer.png)
**Container Layers**, retrieved from the [Docker documentation](https://docs.docker.com/storage/storagedriver/)

- **Challenge of Data Persistence in Containers:**
    - The read-write layer in containers is ephemeral; it is lost when the container is stopped or deleted.
    - Similar to computer memory erasure when shut down.
- **Persistence Through Writing to Disk:**
    - To retain data, it must be written to disk before container shutdown or deletion.
- **Using Volumes for Persistent Data:**
    - Containers can use volumes to achieve data persistence.
    - Concept: Instead of isolating the entire filesystem, specific directories on the host are passed into the container filesystem.
    - While this ensures data persistence, it weakens the isolation of the container as it effectively grants access to the host filesystem.
![Data sharing in containers](../images/sharing_data.png)
Data is shared between two containers on the same host

- **Challenges in Container Orchestration for Data Persistence:**
    - Orchestrating numerous containers introduces challenges beyond persisting data on the host where the container originated.
    - Common scenarios include data access by multiple containers on different host systems or when a container starts on a different host but still requires access to its volume.
- **Role of Container Orchestration Systems (e.g., Kubernetes):**
    - Container orchestration systems, like Kubernetes, can address these challenges.
    - Effective resolution, however, relies on a robust storage system connected to the host servers.
    - The orchestration system facilitates coordination and management, but a reliable storage infrastructure is crucial for seamless data access and sharing across containers and hosts.
![Storage System](../images/storage_system.png)
**Storage is provisioned via a central storage system. Containers 
on Server A and Server B can share a volume to read and write data**

- Standardization for Diverse Storage Implementations:
    - The continuous expansion of various storage solutions prompted the need for a standardized approach.
    - The **[Container Storage Interface (CSI)](https://github.com/container-storage-interface/spec)** was introduced to provide a uniform interface, enabling the attachment of different storage systems.
    - This standardization facilitates seamless integration of diverse storage solutions, whether they are cloud-based or on-premises.

### [**Container Orchestration**](https://kevinsulatra.github.io/k8snotes/kcna_notes/container_orchestration/container_orchestration.html)
