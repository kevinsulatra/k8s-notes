# Interacting with K8s

To interact with the API, users can utilize the official command-line interface, kubectl. Now, let's explore essential commands for everyday Kubernetes tasks. Note: Refer to the [official documentation](https://kubernetes.io/docs/tasks/tools/#kubectl) for kubectl installation instructions.

You can list the available objects in your cluster with the following command:
```
$ kubectl api-resources

NAME                    SHORTNAMES  APIVERSION  NAMESPACED  KIND
...
configmaps              cm          v1          true        ConfigMap
...
namespaces              ns          v1          false       Namespace
nodes                   no          v1          false       Node
persistentvolumeclaims  pvc         v1          true        PersistentVolumeClaim
...
pods                    po          v1          true        Pod
...
services                svc         v1          true        Service 
```

- Objects in Kubernetes have short names, which is particularly beneficial for objects with longer names such as configmaps or persistentvolumeclaims.
- The table provides information about whether an object is namespaced and the version in which it is available.
- For more details about an object, kubectl offers a built-in explanation function.

```
$ kubectl explain pod

KIND:     Pod
VERSION:  v1

DESCRIPTION:
     Pod is a collection of containers that can run on a host. This resource is
     created by clients and scheduled onto hosts. 

FIELDS: 
   apiVersion <string>
     APIVersion defines the versioned schema of this representation of an
     object. Servers should convert recognized schemas to the latest internal
     value, and may reject unrecognized values.
...
   kind <string>
...
   metadata <Object>
...
   spec <Object>
```

To learn more about the pod spec, you can drill down in the object definition. Use the format: `<type>.<fieldName>[.<fieldName>]`
```
$ kubectl explain pod.spec

KIND:     Pod
VERSION:  v1 

RESOURCE: spec <Object>  

DESCRIPTION:
     Specification of the desired behavior of the pod. More info:

https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#spec-and-status

     PodSpec is a description of a pod.

FIELDS:
   activeDeadlineSeconds <integer>
     Optional duration in seconds the pod may be active on the node relative to
     StartTime before the system will actively try to mark it failed and kill
     associated containers. Value must be a positive integer. 

   affinity <object>
     If specified, the pod's scheduling constraints 

   automountServiceAccountToken <boolean>
     AutomountServiceAccountToken indicates whether a service account token
     should be automatically mounted. 

   containers <[]Object> -required-
...
```

Use `--help` flag to view basic `kubectl` commands

```
$ kubectl --help

kubectl controls the Kubernetes cluster manager. 

 Find more information at: https://kubernetes.io/docs/reference/kubectl/overview/ 

Basic Commands (Beginner):
  create Create a resource from a file or from stdin
  expose Take a replication controller, service, deployment or pod and expose it as a new Kubernetes service
  run Run a particular image on the cluster
  set Set specific features on objects 

Basic Commands (Intermediate):
  explain Get documentation for a resource
  get Display one or many resources
  edit Edit a resource on the server
  delete Delete resources by file names, stdin, resources and names, or by resources and label selector
  ```

To create an object in Kubernetes from a YAML file
```
$ kubectl create -f <your-file>.yaml
```
- Various graphic user interfaces and dashboards are available for Kubernetes, providing a visual way to interact with the cluster.
- Additional tools for interacting with Kubernetes include:
  - kubernetes/dashboard
  - derailed/k9s
  - Lens
  - VMware Tanzu Octant
- Despite the abundance of CLI tools and GUIs, there are advanced tools for creating templates and packaging Kubernetes objects.
- Helm is a widely used tool in connection with Kubernetes, serving as a package manager that facilitates updates and object interaction.
- Helm packages Kubernetes objects into Charts, which can be shared via a registry, and users can search ArtifactHub for ready-to-deploy software packages when getting started with Kubernetes.
