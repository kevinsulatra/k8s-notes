# **Characteristics of Cloud Native Architecture**

- High level of automation
- Self healing
- Scalable
- (Cost-) Efficient
- Easy to maintain
- Secure by default

A good baseline and starting point for your cloud native journey is the twelve-factor app. The twelve-factor app is a guideline for developing cloud native applications, which starts with simple things like version control of your codebase, environment-aware configuration, and more sophisticated patterns like statelessness and concurrency of your application.

While these patterns and technologies provide full advantage if they run in the cloud, they can also offer a lot of benefits when applied to on-premises systems. Last but not least, they allow a smoother transition if you migrate your applications and infrastructure to the cloud.

## **High level of automation**

To manage all the moving parts of your cloud-native application, automation is recommended in every step from development to deployment. This can be achieved by using modern automation tools and Continuous Integration/Continuous Delivery (CI/CD) pipelines. CI/CD pipelines are a concept used for the multiple steps involved in delivering a new version of your software and are backed by a version control system like git.

Benefits of automation include:

- Fast, frequent, and incremental changes to production
- Minimal human involvement in building, testing, and deploying applications and infrastructure
- Easier disaster recovery in case of system rebuild

## **Self Healing**

- Applications and infrastructure can fail periodically.
- Cloud native frameworks and infrastructure components have built-in health checks to monitor applications from the inside.
- Health checks enable automatic restart of applications if needed.
- Compartmentalization of applications allows for isolated failures, where only certain parts may stop working or slow down while others remain unaffected.

## **Scalable**

Scaling your application refers to the process of handling increased workload while maintaining a positive user experience. One approach to scaling is running multiple instances of the same application and distributing the workload among them. Automating this process based on application metrics such as CPU or memory usage can further enhance the availability and performance of your services.

## **(Cost-) Efficient**

Just like scaling up your application for high traffic situations, scaling down your application and utilizing usage-based pricing models of cloud providers can save costs if traffic is low. To optimize your infrastructure usage, orchestration systems like Kubernetes can help with more efficient and denser placement of applications.

## **Easy to maintain**

Using Microservices allows applications to be broken down into smaller pieces, which makes them easier to maintain. This approach also makes the applications more portable, easier to test, and enables distribution across multiple teams. By adopting a microservices architecture, organisations can achieve improved maintainability and flexibility in their software systems.

## **Secure by default**

Cloud environments are often shared between multiple customers or teams, which calls for different security models. In the past, a lot of systems were divided into different security zones that denied access from different networks or people. Once you're inside a zone, you can access every system inside. However, this approach poses significant security risks as any compromised system within the zone can potentially access all other systems.

To address this challenge, the concept of "Secure by Default" has emerged. Secure by Default is a principle that emphasizes implementing strong security measures as the default configuration for systems and services. This means that access to resources and data is restricted by default, and each user and process must authenticate themselves before accessing any system or resource.

One of the prominent patterns that aligns with the Secure by Default principle is zero trust computing. Zero trust computing assumes that no user or process should be inherently trusted, regardless of their location or network. Instead, it requires continuous authentication and verification of every user and process, even if they are already inside a trusted zone. By implementing zero trust principles, organisations can significantly mitigate the risks associated with shared cloud environments and ensure that security is prioritised at every level.

Implementing Secure by Default and adopting patterns like zero trust computing are crucial steps in safeguarding cloud environments and protecting sensitive data from unauthorized access and potential breaches.

## **Zero Trust Computing Principles**

- Zero trust computing assumes that no user or process should be inherently trusted, regardless of their location or network.
- It requires continuous authentication and verification of every user and process, even if they are already inside a trusted zone.
- By implementing zero trust principles, organisations can significantly mitigate the risks associated with shared cloud environments.
- Zero trust computing ensures that security is prioritised at every level to protect sensitive data from unauthorized access and potential breaches.

## **The 12 Factor App**

The 12 Factor App is a methodology for building software-as-a-service (SaaS) applications. It was created by developers at Heroku and has become a popular approach for designing and developing modern cloud-native applications.

The 12 Factor App outlines twelve principles or best practices that should be followed when developing software-as-a-service applications. These principles cover various aspects of application development, deployment, and operation, aiming to ensure scalability, maintainability, and portability.

Some of the key principles of The 12 Factor App include:

1. Codebase: One codebase tracked in a version control system, but many deploys.
2. Dependencies: Explicitly declare and isolate dependencies.
3. Config: Store configuration in the environment, not in the code.
4. Backing Services: Treat backing services as attached resources.
5. Build, Release, Run: Strictly separate build and run stages.
6. Processes: Execute the app as one or more stateless processes.
7. Port Binding: Export services via port binding.
8. Concurrency: Scale out via the process model.
9. Disposability: Maximize robustness with fast startup and graceful shutdown.
10. Dev/Prod Parity: Keep development, staging, and production as similar as possible.
11. Logs: Treat logs as event streams.
12. Admin Processes: Run admin/management tasks as one-off processes.

By following The 12 Factor App methodology, developers can create applications that are easier to develop, deploy, and scale. The principles help to promote modularity, scalability, and resilience in modern cloud environments.

### [**Cloud Native Architecture**](https://kevinsulatra.github.io/k8snotes/kcna_notes/cloud_native_architecture/cn_arch.html)
