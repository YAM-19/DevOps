# Virtual Machines (VMs)

## 1. What Is a Server?

A server is a computer system that provides services, data, or applications to other computers over a network.

Examples:
- Web Server – Hosts websites.
- Database Server – Stores and manages data.
- Application Server – Runs application logic.

## 2. Resource Underutilization

Traditionally, organizations used one physical server for one application. However, applications might use only a small portion of the server's CPU and memory.

Problems:
- Wasted hardware resources.
- High infrastructure costs.
- Increased electricity and maintenance expenses.

**Solution:** Virtualization allows multiple virtual machines to run on a single physical server.

## 3. What Is Virtualization?

Virtualization is a technology that allows multiple virtual machines (VMs) to run on a single physical computer.

Benefits:
- Better hardware utilization.
- Reduced infrastructure costs.
- Isolation between virtual machines.
- Flexible resource allocation.
- Faster server provisioning.

## 4. What Is a Virtual Machine?

A Virtual Machine (VM) is a software-based computer that behaves like a physical computer.

Each VM can have its own:
- Operating system.
- CPU and memory allocation.
- Virtual storage.
- Network configuration.

Example:
- VM 1 – Ubuntu Linux for a website.
- VM 2 – Windows Server for a business application.
- VM 3 – Ubuntu Linux for a database.

## 5. What Is a Hypervisor?

A hypervisor is software or firmware that creates and manages virtual machines by allocating physical hardware resources.

### Type 1: Bare-Metal Hypervisor
- Runs directly on physical hardware.
- Commonly used in data centers.
- Examples: VMware ESXi and Xen.

### Type 2: Hosted Hypervisor
- Runs on top of a host operating system.
- Commonly used for learning and testing.
- Examples: Oracle VirtualBox and VMware Workstation.

## 6. Virtualization in AWS

AWS operates large data centers containing physical servers. Virtualization technologies allow AWS to provide computing resources to customers on demand.

Amazon EC2 (Elastic Compute Cloud) provides virtual servers called EC2 instances.

Users can configure:
- Operating system.
- Instance type.
- Storage.
- Networking.

## 7. Advantages of Virtualization

1. Cost reduction.
2. Better resource utilization.
3. Workload isolation.
4. Easier scalability.
5. Flexibility to run different operating systems.
6. Simplified infrastructure management.

## 8. Important Terms

| Term | Meaning |
|---|---|
| Physical Server | Actual computer hardware |
| Virtualization | Creating virtual computing environments |
| Virtual Machine | Software-based computer |
| Hypervisor | Creates and manages VMs |
| EC2 Instance | Virtual server provided by AWS |
| Resource Utilization | Efficiency of resource usage |
| Multi-tenancy | Multiple customers sharing underlying infrastructure with isolation |

## 9. Key Takeaways

- Virtualization allows multiple VMs to run on one physical server.
- Each VM behaves like an independent computer.
- A hypervisor manages virtual machines.
- AWS EC2 provides virtual servers on demand.
- Virtualization improves resource utilization and can reduce costs.

**Connection to DevOps:** Virtual machines are an important foundation for cloud computing, Linux administration, Docker, and Kubernetes.
