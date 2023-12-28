# Building Container Images

- **Container Naming Metaphor:**
    - The term "container" in technology is metaphorically borrowed from standardized shipping containers (ISO 668).
    - Similar to shipping containers, standardized format facilitates stacking, unloading, and transporting with ease.
- **Nautical Theme in Container Technology:**
    - Many terms in the container and cloud-native domain draw from the nautical theme inspired by shipping containers.
- **Docker's Component Reuse:**
    - Docker leverages existing components like namespaces and cgroups to isolate processes.
- **Crucial Breakthrough:**
    - Introduction of container images is pivotal for containers.
    - Container images ensure portability and ease of reuse on diverse systems.
- **Docker's Definition of Container Images:**
    - Docker defines a container image as:

        > “A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.”
        >
- **OCI Image-Spec:**
    - In 2015, Docker's popular image format was contributed to the Open Container Initiative (OCI).
    - Known as OCI image-spec, it's available on GitHub.
    - Images consist of a filesystem bundle and metadata.
![Image Spec](../images/image-spec.png)

- **Container Images:**
    - Images are constructed using a buildfile called Dockerfile.
    - Dockerfile instructions mimic those for installing an application on a server.
- **Example Dockerfile for Python Script:**

    ```docker
    # Base image selection
    FROM ubuntu:20.04

    # Software and libraries installation
    RUN apt-get update && \\
        apt-get -y install python3 python3-pip

    # Copying code to the image
    COPY my-app.py /app/

    # Defining the working directory
    WORKDIR /app

    # Starting process when the container runs
    CMD ["python3","my-app.py"]
    ```

- **Building Image with Docker:**
    - Command for building the image:

        ```bash
        docker build -t my-python-image -f Dockerfile
        ```

    - Parameters:
        - `t my-python-image`: Specifies a name tag for the image.
        - `f Dockerfile`: Specifies the location of the Dockerfile.
- **Dependency Management by Developers:**
    - Developers manage application dependencies and package it for execution.
    - This approach empowers developers to handle dependencies, ensuring a self-contained and runnable package.
- **Distribution via Container Registry:**
    - Images can be distributed using a container registry, a web server for uploading and downloading images.
    - Docker provides built-in commands for pushing and pulling images from the registry:

      ```bash
      docker push my-registry.com/my-python-image
      docker pull my-registry.com/my-python-image
      ```

### [**Container Orchestration**](https://kevinsulatra.github.io/k8snotes/kcna_notes/container_orchestration/container_orchestration.html)
