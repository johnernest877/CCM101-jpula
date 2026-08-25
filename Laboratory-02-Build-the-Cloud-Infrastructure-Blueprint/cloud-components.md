# Cloud Infrastructure Components

This document identifies and explains the major cloud infrastructure components observed in the KillerCoda Ubuntu 24.04 Linux environment used for this lab.

## 1. Compute Resources

**What it is:** The CPU (processor cores) and RAM allocated to the virtual machine — observed via `lscpu` and `free -h` in Checkpoint 2.

**Purpose:** Compute resources provide the processing power and memory needed to run applications, execute code, and handle workloads.

**Why it matters in cloud computing:** In cloud platforms (AWS EC2, Azure VMs, GCP Compute Engine), compute is offered as scalable, on-demand virtual instances. Customers pay only for the CPU/RAM they use, and can scale up or down instantly instead of buying physical hardware.

**Relation to KillerCoda:** The KillerCoda playground itself *is* a compute resource — a temporary virtual machine provisioned in the cloud, giving us CPU cores and RAM to run Linux commands, just like a small EC2 instance would.

## 2. Storage Resources

**What it is:** The disk capacity and mounted file systems observed via `df -h`.

**Purpose:** Storage holds the operating system files, user data, and any files created during the session persistently (for the life of the container) on disk.

**Why it matters in cloud computing:** Cloud storage (AWS S3/EBS, Azure Blob/Disk Storage, GCP Cloud Storage/Persistent Disk) lets organizations store data without managing physical drives, with built-in redundancy and scalability.

**Relation to KillerCoda:** The root filesystem (`/`) mounted on the container acts as our block storage — comparable to an EBS volume attached to an EC2 instance.

## 3. Networking Resources

**What it is:** The hostname and IP address observed via `hostname` and `hostname -I`.

**Purpose:** Networking connects the server to other machines and the internet, enabling communication, remote access, and service exposure.

**Why it matters in cloud computing:** Cloud networking (AWS VPC, Azure Virtual Network, GCP VPC) lets engineers control how instances communicate — defining subnets, firewalls, and public/private access.

**Relation to KillerCoda:** KillerCoda assigns the container a private IP address and hostname, simulating how a cloud VM sits inside a provider's internal network before any public IP or load balancer is attached.

## 4. Operating System

**What it is:** Ubuntu 24.04 LTS, identified via `uname -r`.

**Purpose:** The OS manages hardware resources, runs processes, and provides the environment in which all cloud services and applications execute.

**Why it matters in cloud computing:** Every cloud compute instance runs on top of an OS image. Choosing the right OS affects compatibility, security patching, licensing cost, and available tooling.

**Relation to KillerCoda:** The playground boots a minimal Ubuntu image, similar to selecting an AMI (Amazon Machine Image) or OS disk image when launching a cloud VM.
