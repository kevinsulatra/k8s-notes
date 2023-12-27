# Kubernetes Objects

One of the core concepts of Kubernetes is providing a variety of mostly abstract resources, referred to as objects, to describe how your workload should be handled. These objects serve different purposes, from handling container orchestration challenges like scheduling and self-healing to addressing inherent problems of containers.

Kubernetes objects can be categorized into two main types:
- **Workload-oriented objects:** Used for handling container workloads.
- **Infrastructure-oriented objects:** Handle configuration, networking, and security, among other aspects.

Some objects can be organized into a namespace, while others are available across the entire cluster.

As a user, you can define these objects in the YAML data-serialization language and send them to the API server for validation and creation. Here's an example YAML snippet for a Deployment object:

```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
spec: 
  selector:
    matchLabels:
      app: nginx
  replicas: 2 # tells deployment to run 2 pods matching the template
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.19
        ports:
        - containerPort: 80
```
The fields highlighted in red are required fields, including:

`apiVersion`: Specifies the version of the object.

`kind`: Defines the type of object to be created.

`metadata`: Contains data used for identification. A unique name is required for each object.

`spec`: Specifies the desired state of the object. Note that the structure can change with the object's version.

It's crucial to understand that creating, modifying, or deleting an object in Kubernetes is a record of intent. You describe the state your objects should be in, but you're not actively starting pods or containers. Unlike local development, you won't receive direct feedback on whether it worked or not.
