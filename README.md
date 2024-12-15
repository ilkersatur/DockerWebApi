# The Limitations of Physical Server Systems and Transition to Virtualization

<img src="https://github.com/ilkersatur/DockerWebApi/blob/main/Note/system.png" align="left"/>
<img src="https://github.com/ilkersatur/DockerWebApi/blob/main/Note/server.png" align="left"/>

## Main Issues with Physical Systems

- **Scalability**: Adding and managing new servers becomes challenging as workloads increase.  
- **Management Complexity**: Managing, updating, and troubleshooting numerous servers requires significant time and expertise.  
- **Cost**: Purchasing new hardware and maintaining existing systems is expensive.  
- **Risk of Downtime**: A failure in a single server can impact the entire system.  
- **Update Challenges**: Updating all servers in the system is a lengthy and risky process.

<img src="https://github.com/ilkersatur/DockerWebApi/blob/main/Note/remote.png" align="left"/>

## Virtualization as a Solution

Virtualization allows a single physical server to be divided into multiple virtual machines, providing the following benefits:

- **Efficient Resource Usage**: Physical resources are utilized more effectively.  
- **Flexibility**: Systems can be scaled up or down easily.  
- **Ease of Management**: Virtual machines can be centrally managed.  
- **Rapid Deployment**: New applications can be deployed quickly.  
- **Reduced Downtime Risk**: If one virtual machine fails, others remain unaffected.  

---

# Advantages and Disadvantages of Virtualization

## Advantages

- **Ease of Management**: Simplifies system management by running multiple virtual machines on a single physical machine. Tasks like creating, deleting, and cloning virtual machines are quick and practical.  
- **Flexibility**: Enables running different operating systems and applications simultaneously. This facilitates setting up test environments and checking compatibility between software.  
- **Cost Savings**: Reduces the need for physical servers, saving energy and cooling costs.  
- **Security**: Virtual machines are isolated from the physical machine, minimizing potential security risks. Issues in one virtual machine do not affect others.  
- **Fast Backup and Recovery**: Snapshots of virtual machines allow for quick restoration in case of a problem.  

## Disadvantages

- **Resource Usage**: Each virtual machine requires its own operating system and applications, leading to inefficient use of resources, especially in large systems.  
- **Complexity**: Managing large-scale virtualization environments is challenging without automation tools. Thousands of virtual machines require additional effort and expertise.  
- **Update Processes**: Updating virtual machines requires careful planning to avoid disruptions, particularly in systems actively used by users.  

---

# Conclusion

Virtualization is a powerful technology that simplifies computer systems' management and enhances flexibility. However, it also has drawbacks, such as management complexity and resource utilization inefficiency, especially in large-scale systems. Before adopting virtualization technology, it is crucial to evaluate the system's needs and scale carefully.

---

# Fundamentals of Docker's Operation and Architecture

<img src="https://github.com/ilkersatur/DockerWebApi/blob/main/Note/docker.png" align="left"/>

## What Docker Does

Docker is a tool for running applications in isolated environments called **containers**.  

## Docker Architecture

<img src="https://github.com/ilkersatur/DockerWebApi/blob/main/Note/docker-container-images.png" align="left"/>

Communication between the **Docker client** and **Docker daemon** occurs via a REST API. Commands from the client are processed by the daemon.  

## Key Docker Components

- **Docker Images**: Packaged structures containing all components required for an application to run (operating system, libraries, application files).  
- **Docker Containers**: Isolated environments where images are executed.  
- **Docker Hub**: A repository of ready-made Docker images.  

## Common Docker Commands

- `docker pull`: Downloads an image from Docker Hub or another registry.  
- `docker run`: Creates and runs a container from a downloaded image.  
- `docker build`: Creates an image from a Dockerfile.  

## Docker Volumes

Persistent storage areas for container data.  

---

# How Docker Works

1. A Docker image is selected or created.  
2. A container is created from this image.  
3. The container is run, and the application starts running inside the container.  

<img src="https://github.com/ilkersatur/DockerWebApi/blob/main/Note/dockerlocal.png" align="left"/>

## Example Commands

- **Build a Docker Image**:  
  ```bash
  docker build -f Dockerfile -t dockerwebapi:1.0 .
  ```

   ```bash
  docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres
  ``` 
