# Kubernetes the Hard Way with Vagrant

This repository provides a **Vagrantfile** to automate the setup of virtual machines required for **[Kubernetes the Hard Way](https://github.com/kelseyhightower/kubernetes-the-hard-way)** by Kelsey Hightower.

## Why Use Vagrant?

Setting up the virtual machines manually can be time-consuming and complex, especially for those not deeply familiar with virtualization. To simplify this process for students and professionals, I've created a Vagrantfile that automates the provisioning of the necessary environment. This allows you to focus on learning Kubernetes without the overhead of manual VM configuration.

## Prerequisites

- **Mac with ARM architecture**
- **Vagrant** installed
- **VMware Desktop plugin** for Vagrant

## Installation Instructions

1. **Install Vagrant**

   ```bash
   brew tap hashicorp/tap
   brew install hashicorp/tap/hashicorp-vagrant
   ```

2. **Install VMware Desktop Plugin for Vagrant**

   ```bash
   vagrant plugin install vagrant-vmware-desktop
   ```

3. **Clone the Repository**

   ```bash
   git clone https://github.com/azalio/kubernetes-the-hard-way.git
   cd kubernetes-the-hard-way
   ```

4. **Start the Virtual Machines**

   ```bash
   vagrant up
   ```

   This command will create **four virtual machines** configured according to the requirements of Kubernetes the Hard Way.

## Included Files

- **Vagrantfile**: Automates the setup of the virtual machines.
- **encryption-config.yaml**: Necessary for completing the practice as of November 2024.

## Getting Started

With the virtual machines up and running, you can proceed with the steps outlined in Kelsey Hightower's Kubernetes the Hard Way tutorial.

## Feedback and Contributions

Feel free to open issues or submit pull requests if you have suggestions or encounter any issues.

## Why I Created This

As part of developing an advanced Kubernetes course for senior engineers, I recognized the need for hands-on practice. Manually assembling a Kubernetes cluster provides invaluable insights but can be daunting without the right setup. By automating the virtual machine provisioning with Vagrant, I aimed to:

- **Reduce Setup Time**: Eliminate the hassle of manual VM configuration.
- **Enhance Learning**: Allow learners to focus on Kubernetes concepts rather than infrastructure setup.
- **Facilitate Teaching**: Provide a consistent environment for all students in the course.

---

Let's make Kubernetes the Hard Way more accessible and focus on mastering the essentials!

## Kubernetes The Hard Way

This tutorial walks you through setting up Kubernetes the hard way. This guide is not for someone looking for a fully automated tool to bring up a Kubernetes cluster. Kubernetes The Hard Way is optimized for learning, which means taking the long route to ensure you understand each task required to bootstrap a Kubernetes cluster.

> The results of this tutorial should not be viewed as production ready, and may receive limited support from the community, but don't let that stop you from learning!

## Copyright

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.


## Target Audience

The target audience for this tutorial is someone who wants to understand the fundamentals of Kubernetes and how the core components fit together.

## Cluster Details

Kubernetes The Hard Way guides you through bootstrapping a basic Kubernetes cluster with all control plane components running on a single node, and two worker nodes, which is enough to learn the core concepts.

Component versions:

* [kubernetes](https://github.com/kubernetes/kubernetes) v1.28.x
* [containerd](https://github.com/containerd/containerd) v1.7.x
* [cni](https://github.com/containernetworking/cni) v1.3.x
* [etcd](https://github.com/etcd-io/etcd) v3.4.x

## Labs

This tutorial requires four (4) ARM64 based virtual or physical machines connected to the same network. While ARM64 based machines are used for the tutorial, the lessons learned can be applied to other platforms.

* [Prerequisites](docs/01-prerequisites.md)
* [Setting up the Jumpbox](docs/02-jumpbox.md)
* [Provisioning Compute Resources](docs/03-compute-resources.md)
* [Provisioning the CA and Generating TLS Certificates](docs/04-certificate-authority.md)
* [Generating Kubernetes Configuration Files for Authentication](docs/05-kubernetes-configuration-files.md)
* [Generating the Data Encryption Config and Key](docs/06-data-encryption-keys.md)
* [Bootstrapping the etcd Cluster](docs/07-bootstrapping-etcd.md)
* [Bootstrapping the Kubernetes Control Plane](docs/08-bootstrapping-kubernetes-controllers.md)
* [Bootstrapping the Kubernetes Worker Nodes](docs/09-bootstrapping-kubernetes-workers.md)
* [Configuring kubectl for Remote Access](docs/10-configuring-kubectl.md)
* [Provisioning Pod Network Routes](docs/11-pod-network-routes.md)
* [Smoke Test](docs/12-smoke-test.md)
* [Cleaning Up](docs/13-cleanup.md)
