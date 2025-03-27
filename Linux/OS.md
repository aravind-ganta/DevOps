### Operating System (OS)

**What is an Operating System?**
OS is a software managing...
* computer hardware,
* software resources
* and provides common services for computer programs

OS as abstraction layer between applications and hardware
* Instead of applications (like browser) interacting with the computer hardware directly, they can use the OS as abstraction layer between the two
* Messy, if every app had to talk directly to the hardware parts
* Apps, like browser can't be installed directly on the hardware

**Tasks of an Operating System**
1. **Resource Allocation and Management** 
* OS manages resources among applications:
  * Process Management (CPU) :
      * 1 CPU can only process 1 task at a time
      * OS decides which process gets the processor (CPU), when and for how much time and allocates the processor to the process
      * CPU is switching so fast that you don't notice it
  * Memory Management (RAM):
      * Allocating working memory (RAM = Rapid Access Memory) to applications
      * RAM is limited on the computer
  * Storage Management (Hard Drive) :
      * Also called "secondary memory" - the hard drive
      * Persisting data long-term, like files, browser configurations, games, pictures, videos etc.
2. **File Management**
  * Files are stored in structured way
  * A file system is organized into directories
     * On Unix system: tree file system
     * On Windows OS: multiple root folders
3. **Device Management**
  * Manages device communication via their respective drivers
  * Activities like:
      * Keeping track of all devices
      * Deciding which process gets the device, when and how long
4. **Other important tasks**
**Security:**
  * Managing Users and Permissions
  * Each user has its own space and permissions
**Networking**
  * Ports and IP addresses
  * Transmitting outgoing data from all application ports onto the network, and forwarding arriving network packets to processes 

### Operating System Components

**Kernel**
  * Heart of every OS
  * The core program that provides basic services for all other parts of the OS
  * Consists of device drivers, dispatcher, scheduler, file system etc.
  * One of the first programs loaded on startup
  * Controls all hardware resources via device drivers
  * Kernel starts the process for app
  * Allocates resources to app
  * Cleans up the resources when app shuts down

**Application Layer**
  * On top of Kernel is the application layer
  * For example different Linux distributions: Ubuntu, Mint, CentOS, Debian
  * Different application layers, but based on same Linux kernel
  * Android is also based on Linux kernel
  * Linux Kernel most widely used
  * MacOS and iOS is based on a different Kernel

**How to interact with Kernel**
* Graphical User Interface
* Command Line Interface

**3 Main Operating Systems:**
* Linux
* Windows
* MacOS

Each OS has many versions. But kernel stays the same!

**Client OS vs Server OS**
**Client OS**
  * For personal computers with GUI and I/OS devices

**Server OS**
  * Linux and Windows have server distributions
  * But Linux most widely used
  * More light-weight and performant
  * No GUI or other user applications

**MacOS vs Linux**
  * MacOS and Linux: Command Line, File structure etc. similar
  * Whereas Windows is completely different

**UNIX(1970)**
  * Codebase for many different OS
  * Developed independent of Linux
  * Many OS built on top of Unix
  * MacOS Kernel is based on Unix
  * To keep them compatible, standards were introduced
  * POSIX (Portable Operating System Interface) is the most popular standard

**Linux (1991)**
  * Linux was developed in parallel to Unix based operating systems
  * No source code of UNIX
  * Created by Linus Torvalds
  * Clone of UNIX or also called "unix like"
  * Linux and MacOS both POSIX compliant
  
**Why learn Linux as a DevOps Engineer**
  * Linux is mostly used OS for servers!
  * Knowing Linux is a must for DevOps Engineers
      * you need to work with servers
      * installing and configuring servers
      * Linux native technologies





