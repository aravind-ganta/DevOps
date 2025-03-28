### Introduction to Package Manager

### How to install software

**On Windows**
  * On Windows you have download installer
  * Wizards that guide you through the installation

**On Linux**
  * On Linux you will install applications mostly with package manager tools on CLI

#### What is a software package?
  * A compressed archive, containing all required files for the software to run
  * Apps usually have dependencies, which needs to be installed with it
  * Files are split across different folders

#### Tasks of a Package Manager
  * Downloads, installs or updates existing software from a repository
  * Ensures the integrity and authenticity of the package
  * Manages and resolves all required dependencies
  * Knows where to put all the files in the Linux file system
  * Easy upgrading of the software

#### Package Manager - pre-installed
* Package Manager is already included in every Linux distribution
* On Ubuntu, you have APT package manager available
> APT = Advanced Package Tool
* Package Manager like apt has commands you can use to install uninstall orPulls the latest changes from the APT repositories upgrade software

#### Package Repository
* A repository is a storage location, where all the software packages are hosted
* Contains thousands of programs
* Package Manager fetches the packages from these repositories
> Always update the package index before upgrading or installing new packages
> "sudo apt update"
* Pulls the latest changes from the APT repositories
* The APT package index is basically a database
* Holding records of available packages from the repositories

#### Alternative Package Manager
* There are different package manager available
* A very similar package manager is APT-GET, which you will often come across

#### APT
* Is more user friendly, like progress bar
* Fewer, but sufficient command options in a more organized way
* Recommended by Linux distributions!

#### APT-GET
* On Ubuntu, APT-GET also out of the box available
* Different set of commands
* You can achieve the same user friendly output, if you use additional command options
> E.g. "apt search" not available
* On Linux you will mostly use apt package manager
* But generally, you need to know different ways to install a software

#### Why?
* When there are packages, that are not available in these
official repositories
* Or package is available, but not the latest version (software
packages are verified, before adding to repository and
verification process takes time)
* Programs, which are not available: Browsers, Code editors
etc.

### Alternative ways to install software
#### Ubuntu Software Center
* Like an app store
* A utility for installing, purchasing, removing software in Ubuntu
* Has a graphical UI, so no need for using the CLI:

#### Snap Package Manager
* Snap is a software packaging and deployment system
* A newer package manager, initial release in 2014
* Many still use the term "snappy", which it was called before
* A package manager for all OS, which use the Linux kernel

### Snap vs APT
#### Snap
* Self-contained - dependencies contained in the package
* Supports universal Linux packages (package type .snap)
* Automatic Updates
* Larger Installation size

#### APT
* Dependencies are shared
* Only for specific Linux distributions (package type .deb)
* Manual Updates
* Smaller Installation size

### Add repository to official list of repos
#### Use Case:
* When installing relatively new applications, which are not yet
in the official repositories
#### How to:
* Add the repository, which contains the package to official
repositories list
* Often the command is listed in the installation guide of the
tool:
```
sudo add-apt-repository "deb [arch=$(dpkg --print-architecture)] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```
* Command adds repository to APT sources (into
/etc/apt/sources.list)
* Afterwards, you can install the package as usual - the next apt
install will look into this new repository as well

#### PPA = Personal Package Archive
* Some of these repositories are PPA 
* PPAs are provided by the community
* Private repository to distribute the software - anybody can create it
* Usually used by developers to provide updates more quickly than in the official Ubuntu repositories
* Be aware of possible risks before adding a PPA
    * No guarantee of quality or security
    * Can cause difficulties e.g. when upgrading to a new Ubuntu release

### Linux Distributions
* Linux Distros grouped, based on same source code 
* Distros in same category, use the same package manager

#### Debian based (APT)
* Ubuntu
* Debian
* Mint

#### Red Hat based (YUM)
* RHEL
* CentOS
* Fedora

#### Similar concept:
* Package Manager uses official repositories
* Downloads packages, resolves dependencies etc
#### Difference of Repositories:
* More or newer versions of packages

#### Decision which Linux Distro to use
* Sys admins decide on Linux distributions they install based on package manager
* Within same category the difference is very small