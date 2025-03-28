### Virtualization & Virtual Machine

**What is Virtualization and a Virtual Machine**
  * Virtual Machine is commonly shortened to just "VM"
  * VM is a virtual computer running on top of another host computer

**How it works - Virtualization**
  * Virtualization is the process of creating a software-based, or "virtual" version of a computer, with dedicated amounts of CPU, memory, and storage that are "borrowed" from a physical host computer
  * Makes it possible that any OS can run on top of any other physical host machine
  * The VM is partitioned from the rest of the system, meaning it's completely isolated and can't interfere with the host computer's primary OS

**Hypervisor**
  * The essential component in the virtualization stack is a piece of software called a hypervisor
  * One of the most popular hypervisor is open-source Oracle VM VirtualBox

**Host OS vs Guest OS**
  * Host OS = runs directly on the hardware
  * Guest OS = runs on the virtual machine
The hardware resources are shared So you can only give resources you actually have

**Type 1 - Native or Bare Metal**
  * That run directly on the host's hardware to control the hardware, and to monitor the guest OS. The guest OS runs on a separate level above the hypervisor
  * Examples of this classic implementation of VM architecture are Oracle VM, Microsoft Hyper-V, VMware ESXi.

**Type 1 - Use Cases**
  * Efficient usage of hardware resources (e.g. cloud provider):
      * Use all the resources of a performant big server
      * Users can choose any resource combinations

**Type 2 - Hosted**
  * Designed to run within a traditional OS
  * A hosted hypervisor adds a distinct software layer on top of the host OS, and the guest OS becomes a third software level above the hardware
  * Examples: Oracle VM VirtualBox, VMware Server, Microsoft Virtual PC, KVM, QEMU and Parallels.

**Type 2 - Use Cases**
  * Learn and experiment:
      * You don't need to buy a new computer for that
      * You don't endanger your main OS
  * Test your app on different OS
  * Backing up your existing OS

**Why companies adopt Virtualization**

Main benefit: Instead of OS being tightly coupled to the hardware, Virtualization gives an abstraction layer, with the following benefits:
  * Security: Secure very easily
  * Agility and speed: Spinning up a VM is easy and quick, compared to setting up an entire new server
  * Cost savings: Efficient usage of hardware resources
  * Portable: OS as a portable file (VMI - Virtual Machine Image)
      * VMI:
        * Includes OS and all applications on it
        * You can have backups of your entire OS

**Setup Linux VM**
  1. Install VirtualBox Hypervisor
  2. Setup Linux Ubuntu Virtual Machine