# Running Containers

- **OCI Runtime-Spec and runC:**
    - Industry-standard containers don't necessitate Docker; OCI runtime-spec can be followed.
    - Open Container Initiative (OCI) maintains the runC reference implementation, a low-level runtime utilized by various tools, including Docker.
- **Container Image vs. Running Container:**
    - Analogous to object-oriented programming: container image is like a class, and the running container is its instantiation.
- **Docker Commands:**
    - With Docker installed, containers can be started using commands like:

        ```bash
        docker run nginx
        ```

- **Runtime-Spec and Image-Spec Relationship:**
    - Runtime-spec complements image-spec, covered in the next chapter.
    - Describes container image unpacking and manages the complete container lifecycle, from creation to process start, stop, and deletion.
- **Local Machine Alternatives:**
    - Numerous alternatives for local machine use:
        - Some for building images (e.g., buildah, kaniko).
        - Others, like podman, serve as full alternatives to Docker.
- **Podman Features:**
    - Podman, a Docker alternative, provides a similar API.
    - Additional features include running containers without root privileges and introducing the Pod concept, explored later.

### [**Container Orchestration**](https://kevinsulatra.github.io/k8snotes/kcna_notes/container_orchestration/container_orchestration.html)
