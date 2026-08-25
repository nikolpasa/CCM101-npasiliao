# Cloud Infrastructure Components

## 1. Compute Resources
### Purpose
Compute resources are the processing power of a system — the CPU and RAM that actually run programs, execute instructions, and handle calculations. In a cloud environment, compute is the "brain" that takes a request and does something with it, whether that's running a web server, processing data, or executing a script.

### Importance in Cloud Computing
Compute is one of the core building blocks of any cloud service. Every virtual machine, container, or application depends on allocated CPU and memory to function. In cloud computing, compute resources can be scaled up or down on demand, which lets organizations pay only for the processing power they actually need instead of maintaining physical hardware that may sit idle.

### KillerCoda Example
In the KillerCoda Ubuntu environment, the `lscpu` output showed a single virtual CPU (Intel Xeon E312xx, Sandy Bridge, IBRS update, 1 core, 1 thread), running under a KVM hypervisor with full virtualization. This is a good example of how cloud compute works: the "CPU" here isn't a dedicated physical chip, it's a virtualized slice of a larger host machine's processor. Likewise, `free -h` showed 1.9 GiB of total RAM, which is the memory budget the container/VM has to run all its processes — small on purpose, since it's a lightweight lab environment rather than a production server.

## 2. Storage Resources
### Purpose
Storage resources are where data is kept — files, databases, logs, application code, and the operating system itself all live on some form of disk storage. Storage provides the persistence that compute lacks on its own, since RAM is wiped when a process or machine stops, but disk storage retains data.

### Importance in Cloud Computing
Cloud storage needs to be reliable, scalable, and separable from compute so data can persist independently of any single virtual machine. This is why cloud providers offer storage as its own service (block storage, object storage, file storage) — it lets you resize, back up, or move storage without touching the compute resources attached to it, and it protects data if a compute instance fails or is replaced.

### KillerCoda Example
The Linux environment provides disk storage that can be examined using `df -h`. In this lab, the root filesystem (`/dev/vda1`) had a 19G capacity, with 5.4G used and 13G available (30% utilization). Separate small partitions like `/dev/vda16` (mounted at `/boot`) and `/dev/vda15` (mounted at `/boot/efi`) show how storage is often split into multiple partitions for different purposes even within a single virtual disk.

## 3. Networking Resources
### Purpose
Networking resources are what connect a system to other systems — other servers, the internet, or users. This includes network interfaces, IP addresses, routing, and the rules that control what traffic is allowed in or out. Without networking, a compute resource would be isolated and unreachable.

### Importance in Cloud Computing
Networking is what makes "the cloud" actually cloud-like — it's the layer that lets a user's request travel from their device, across the internet, to a compute resource, and back. In cloud computing, networking also enforces security boundaries (firewalls, security groups) and determines how resources communicate with each other internally, which is critical for both accessibility and protection against unauthorized access.

### KillerCoda Example
In the lab environment, the `hostname` command returned `ubuntu` as the system's network identity, and `hostname -I` returned the IP addresses `172.30.1.2` and `172.17.0.1`. The `ip -br addr` output showed the actual interfaces behind those addresses: `enp1s0` (UP, assigned `172.30.1.2/24`) is the machine's main network interface connecting it to the rest of the playground's network, while `docker0` (DOWN, `172.17.0.1/16`) is a virtual bridge interface Docker sets up for container networking, and `lo` is the loopback interface used for the machine to talk to itself. Together these show how even a single lab VM has multiple network paths, similar to how cloud instances often have separate interfaces for public, private, and internal container traffic.

## 4. Operating System
### Purpose
The operating system is the software layer that manages hardware resources (CPU, memory, disk, network) and provides the environment in which applications actually run. It handles process scheduling, file systems, permissions, and the interface between hardware and software.

### Importance in Cloud Computing
The OS is what turns raw compute, storage, and networking into something usable. In cloud computing, the operating system image is typically what you select or configure when provisioning a virtual machine, and it determines what tools, package managers, and security models are available. Linux distributions dominate cloud infrastructure because they're lightweight, scriptable, and well-suited to automation.

### KillerCoda Example
The laboratory environment uses Ubuntu 24.04. Details confirmed from `/etc/os-release` and `uname -r` — `VERSION="24.04.4 LTS (Noble Numbat)"` running kernel `6.8.0-13-generic` — show a standard long-term-support Linux distribution, the same kind of OS commonly deployed on cloud virtual machines because of its stability and long support window.
