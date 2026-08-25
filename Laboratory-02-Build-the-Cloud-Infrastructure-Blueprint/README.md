# Technical Documentation

## Mission Overview

Congratulations,
Your onboarding has been successfully completed, and your Cloud Computing Portfolio has been approved by your supervisor.
CloudNova Technologies has now assigned you to your first official project.
Before deploying cloud services, every cloud engineer must understand the infrastructure that powers modern cloud computing. Your mission is to investigate the components of cloud infrastructure, identify how compute, storage, networking, and identity services work together, and document your findings as if you were preparing technical documentation for a client.

## Objectives

The objectives of this laboratory activity were to:

* Explain the major components of cloud infrastructure.
* Investigate the hardware and software resources available in a Linux environment.
* Differentiate compute, storage, networking, and identity resources.
* Interpret the relationship between cloud infrastructure components.
* Create professional technical documentation using Markdown.
* Continue building a structured GitHub Cloud Computing Portfolio.

## Cloud Infrastructure Components

The main cloud infrastructure components identified in the KillerCoda environment were:

### Compute Resources
The server uses an **Intel Xeon E312xx virtual CPU** with **1 available CPU core**. Compute resources provide the processing power required to execute commands, run applications, and process data.

### Storage Resources
The primary storage resource identified is the **`/dev/vda1`** partition with a capacity of approximately **19 GB**. Storage resources provide space for the operating system, applications, configuration files, and other data.

### Networking Resources
The server has network connectivity through the IP addresses **`172.30.1.2`** and **`172.17.0.1`**. The hostname of the server is **`ubuntu`**. Networking resources allow the server and other resources to communicate with each other and with external networks.

### Operating System
The server runs **Ubuntu 24.04.4 LTS (Noble)** with Linux kernel version **`6.8.0-138-generic`**. The operating system manages and coordinates the available compute, memory, storage, and networking resources.

## Tools Used

The following tools were used during the laboratory activity:

* KillerCoda Playground
* Ubuntu Linux Terminal
* Git
* GitHub
* draw.io
* Markdown

## Linux Commands Executed

The following Linux commands were used to create, navigate, inspect, and document the cloud environment.

### Directory and File Commands
```bash
cd ~/CCM101-cbadongen
mkdir -p Laboratory-02-Build-the-Cloud-Infrastructure-Blueprint
cd Laboratory-02-Build-the-Cloud-Infrastructure-Blueprint
mkdir screenshots
touch README.md infrastructure-report.md cloud-components.md cloud-provider-comparison.md reflection.md
pwd
ls -la
ls -la screenshots
